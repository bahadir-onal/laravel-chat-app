# Chat Uygulaması
 ## Proje Açıklaması


Bu proje, iki kişinin gerçek zamanlı olarak birbirlerine mesaj göndermesine olanak tanıyan bir web tabanlı chat uygulamasını içermektedir. Günümüzün hızla değişen iletişim dünyasında, insanlar arasındaki iletişim artık sadece metin mesajlarıyla sınırlı değil, aynı zamanda bu iletişim gerçek zamanlı ve anında olmalıdır. Bu chat uygulaması, kullanıcıların kolayca kaydolmalarına, oturum açmalarına ve birbirleriyle gerçek zamanlı iletişim kurmalarına olanak tanır.

## Teknolojiler
 Bu proje aşağıdaki teknolojileri kullanmaktadır:
-  **Laravel (Backend PHP Framework)**:  Web uygulamasının temelini oluşturan güçlü bir PHP framework. 
-  **Laravel Sanctum (Authentication Package)**: Kullanıcı kimlik doğrulama ve yetkilendirme için kullanılan paket. 
-  **Jetstream Inertia (Front/Back end user authentication scaffolding)**: Kullanıcı kaydı ve oturum yönetimi için kullanılan arayüz ve back-end yapı. 
-  **Vue.js (Frontend Javascript Framework)**: Arayüzün geliştirilmesinde kullanılan JavaScript çerçevesi. 
-  **Pusher (Real-time web-socket connections)**: Gerçek zamanlı sohbet iletişimini desteklemek için kullanılan WebSockets hizmeti.
 
 ## Depoyu bilgisayarınıza klonlayın. 
`git clone https://github.com/bahadir-onal/laravel-chat-app.git`

`cd proje-adı `

`composer install `

`cp .env.example .env `

`php artisan key:generate `
# .env dosyasını düzenleyerek veritabanı bağlantı ayarlarını yapın 
`php artisan migrate`

`php artisan seed`

# Pusher ayarlarını düzenleyin. `.env` dosyanızdaki aşağıdaki satırları düzenleyin ve Pusher kimlik bilgilerinizi ekleyin:

`BROADCAST_DRIVER=pusher`

`PUSHER_APP_ID=your-app-id`

`PUSHER_APP_KEY=your-app-key`

`PUSHER_APP_SECRET=your-app-secret`

`PUSHER_APP_CLUSTER=your-app-cluster`

# Projeyi çalıştırın

`php artisan serve`



# Katkıda Bulunma:

Eğer projeye katkıda bulunmak isterseniz, lütfen yeni bir dal oluşturun ve değişikliklerinizi yapın. Daha sonra bir çekme isteği oluşturarak değişikliklerinizi değerlendirmemizi sağlayabilirsiniz.

## İletişim
## bahadironal3@gmail.com

## ENGLİSH


# Chat Application
## Project Description

This project includes a web-based chat application that allows two individuals to send messages to each other in real-time. In today's rapidly changing communication landscape, communication is not limited to text messages; it also needs to be real-time and instant. This chat application enables users to easily register, log in, and communicate with each other in real-time.

## Technologies
This project uses the following technologies:
- **Laravel (Backend PHP Framework)**: A powerful PHP framework that forms the foundation of the web application.
- **Laravel Sanctum (Authentication Package)**: A package used for user authentication and authorization.
- **Jetstream Inertia (Front/Back end user authentication scaffolding)**: An interface and back-end structure used for user registration and session management.
- **Vue.js (Frontend JavaScript Framework)**: A JavaScript framework used for developing the user interface.
- **Pusher (Real-time web-socket connections)**: A WebSockets service used to support real-time chat communication.

## Clone the Repository
`git clone https://github.com/bahadir-onal/laravel-chat-app.git`

`cd project-name`

`composer install`

`cp .env.example .env`

`php artisan key:generate`
# Edit the .env file to set up the database connection
`php artisan migrate`

`php artisan seed`

# Configure Pusher settings. Edit the following lines in your `.env` file and add your Pusher credentials:
`BROADCAST_DRIVER=pusher`

`PUSHER_APP_ID=your-app-id`

`PUSHER_APP_KEY=your-app-key`

`PUSHER_APP_SECRET=your-app-secret`

`PUSHER_APP_CLUSTER=your-app-cluster`

# Run the Project
`php artisan serve`

# Contribution:

If you'd like to contribute to the project, please create a new branch and make your changes. Then, create a pull request to have your changes reviewed.

## Contact:
## bahadironal3@gmail.com
