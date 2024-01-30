# Project-I
# Follow these steps to set up and run the project on your local machine.
# Prerequisites
Install XAMPP: Download and install XAMPP from https://www.apachefriends.org/index.html.

Install Composer: Download and install Composer from https://getcomposer.org/download/.

Install PHP 8.1: Make sure PHP 8.1 is installed on your machine. You can download it from https://www.php.net/downloads.php.

Set up PHP in Windows: You can follow step-by-step in this video https://www.youtube.com/watch?v=MPRLUd8Pmyo.

# Clone the Project
Open your terminal and run the following command:
    
    git clone https://github.com/hvtheer/demo123.git
# Navigate to Project Folder
Change into the project directory:
    
    cd demo123
# Install Dependencies
Run Composer to install project dependencies:
    
    composer install
# Configure Environment
Copy the .env.example file to create a new .env file:
    
    cp .env.example .env
# Generate the application key:
    
    php artisan key:generate
# Open the .env file in your project folder and update the database configuration with the database name, username, and password:
  
    DB_CONNECTION=mysql

    DB_HOST=127.0.0.1

    DB_PORT=3306

    DB_DATABASE=demo123

    DB_USERNAME=root

    DB_PASSWORD=
# Start XAMPP Servers
Start your XAMPP control panel and click "Start" for Apache and MySQL. Database Setup
Open PHPMyAdmin in your browser by navigating to http://localhost/phpmyadmin.

Create a new database named demo123.

Run Migrations and Seed
Run the following commands to migrate the database and seed it:

    php artisan migrate
    php artisan db:seed
Import Database Data
Import the provided SQL file into the demo123 database:
In PHPMyAdmin, select the demo123 database.
Click on the "Import" tab.
Choose the e-shop.sql file from the database folder and click "Go" to import the data.

Unzip and Replace Storage Folder
Unzip the storage.zip file and replace the existing storage folder with the extracted contents.

    unzip storage.zip
Create Symbolic Link for Storage
Create a symbolic link to make the storage folder accessible from the public directory:

    php artisan storage:link
Run the Laravel Development Server
Start the Laravel development server:

    php artisan serve
Visit http://localhost:8000 in your browser to view the Laravel application.

Now, your Laravel project should be set up and running locally with XAMPP.
