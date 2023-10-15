<template>
    <AppLayout title="Dashboard">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                <chat-room-selection
                    v-if="currentRoom.id"
                    :rooms="chatRooms"
                    :currentRoom="currentRoom"
                    v-on:roomchanged="setRoom( $event )"
                />
            </h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="bg-white overflow-hidden shadow-xl sm:rounded-lg">
                    <message-container :messages="messages" />
                    <input-message 
                        :room="currentRoom"
                        @messagesent="getMessages" />
                </div>
            </div>
        </div>
    </AppLayout>
</template>

<script> 

import AppLayout from '@/Layouts/AppLayout.vue';
import MessageContainer from './messageContainer.vue';
import InputMessage from './inputMessage.vue';
import chatRoomSelection from './chatRoomSelection.vue';
import axios from 'axios';

export default {
    components: {
        AppLayout,
        MessageContainer,
        InputMessage,
        chatRoomSelection
    },

    data: function () {
        return {
            chatRooms: [],
            currentRoom: [],
            messages: []
        }
    },

    methods: {
        getRooms() {
            axios.get('/chat/rooms')
            .then( response => {
                this.chatRooms = response.data; 
                this.setRoom ( response.data[0] );
            })
            .catch( error => {
                console.log( error );
            })
        },
        
        setRoom ( room ){
            this.currentRoom = room;
            this.getMessages();
        },

        getMessages(){
            axios.get('/chat/rooms/' + this.currentRoom.id + '/messages')
            .then(response => {
                this.messages = response.data;
            })
            .catch(error => {
                console.log( error );
            })
        }
    },

    created() {
        this.getRooms();
    }
}

</script>
