# Student Information Chatbot (PHP & MySQL)

This is a complete, database-driven chatbot application built with PHP, MySQL, and JavaScript. It was created as a final year project for the Bachelor of Science in Computer Science program.

The application provides a simple chat interface for students to ask questions about the college. It also includes a secure admin panel for administrators to manage the chatbot's knowledge base.

## 🚀 Features

* **User-Friendly Chat Interface:** A clean and simple chat window for students to interact with the bot.
* **Database-Driven:** All questions and answers are stored in a MySQL database, making them easy to manage.
* **Dynamic Responses:** The chatbot queries the database in real-time to find the best matching answer.
* **Admin Control Panel:** A secure backend where an admin can:
    * Log in with a username and password.
    * Add new question-and-answer pairs.
    * Edit or delete existing responses.
    * View a list of "unanswered questions" that the bot did not understand, allowing the admin to improve the bot's knowledge.
* **System Configuration:** Admins can update the chatbot's name, welcome message, and logo directly from the admin panel.

## 💻 Technology Stack

* **Backend:** PHP
* **Database:** MySQL
* **Frontend:** HTML, CSS, JavaScript, jQuery, Bootstrap

## 🛠️ How to Set Up and Run This Project

To run this project locally, you will need a server environment like XAMPP or WAMP.

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/](https://github.com/)[Your-Username]/[Your-Repository-Name].git
    ```

2.  **Start Your Server:**
    * Start the **Apache** and **MySQL** services in your XAMPP/WAMP control panel.
    * Move the entire project folder into your server's `htdocs` directory (e.g., `C:/xampp/htdocs/`).

3.  **Set Up the Database:**
    * Open `phpMyAdmin` (usually `http://localhost/phpmyadmin`).
    * Create a new database.
    * Select your new database and go to the **"Import"** tab.
    * Upload the `db/sic_db.sql` file to import all the tables and data.

4.  **Configure the Database Connection:**
    * The file `classes/DB_conn.php` is **ignored by Git** for security.
    * You must **create this file manually** inside the `classes/` folder.
    * Paste the following code into it, replacing `"your_db_name"`, `"your_db_user"`, and `"your_db_password"` with your local database credentials.

    ```php
    <?php
    if(!defined('DB_SERVER')){
        define('DB_SERVER','localhost');
    }
    if(!defined('DB_USERNAME')){
        define('DB_USERNAME','your_db_user'); // e.g., 'root'
    }
    if(!defined('DB_PASSWORD')){
        define('DB_PASSWORD','your_db_password'); // e.g., '' (empty)
    }
    if(!defined('DB_NAME')){
        define('DB_NAME','your_db_name'); // The name of the database you created
    }
    ?>
    ```

5.  **Run the Application:**
    * **Chatbot:** Open your browser and go to `http://localhost/Student Information Chatbot`
    * **Admin Panel:** Go to `http://localhost/Student Information Chatbot/admin/`
