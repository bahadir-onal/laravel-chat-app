<template>
    <div>
        <div>
            {{ message.user.name }}: {{ message.message }}
        </div>
    </div>
</template>

<script>
    export default{
        props: ['message']
    }
</script>