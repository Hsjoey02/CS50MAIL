# CS50 Mail
#### Video Demo:  <https://youtu.be/Zb_FLCk9KZE>
#### Description:

CS50 Mail is a web application that allows users to send and receive email messages.
In order to implement this application, you would need to write code using a programming language and a web framework.

The CS50 Mail application is built using Flask, which is a web framework written in Python. Flask allows you to write code that runs on a web server and handles requests from web browsers.

When you write code for CS50 Mail, you will need to define routes that correspond to the various pages of the application. For example, you might define a route for the login page, a route for the inbox page, and a route for the compose page.

Within each route, you will need to write code that performs various tasks, such as displaying information on the page, processing form data, and interacting with a database to retrieve or store information.

For example, when a user composes a new email message, the form data will be sent to the server using HTTP POST method. You will need to write code that extracts the data from the request and stores it in a database. When a user views their inbox, you will need to retrieve the email messages from the database and display them on the page.

The application allows users to send and receive emails, and users must register and log in to use the application.

The application uses a SQLite database to store user information and emails. The users table in the database stores user ID, username (which is the email address), and a hashed password. The emails table stores email ID, sender, recipient, subject, and body.

The application has several routes:

Here is a summary of what each of your functions does:

    inbox(): displays all emails received by the current user
    compose(): allows the user to compose a new email and stores it in the database
    sent(): displays all emails sent by the current user
    login(): allows the user to log in
    logout(): logs out the user
    email(): displays the details of a specific email
    register(): allows the user to register for an account and store their information in the database

To handle sessions, templates, and forms, the application uses several Flask extensions, including Flask-Login for user authentication, Flask-WTF for form handling and validation, and Flask-Mail for sending emails.

In terms of security, the application uses Flask's built-in session management to store user information, and it uses the Werkzeug library to hash and verify passwords. The application also uses CSRF protection to prevent cross-site request forgery attacks. To prevent SQL injection attacks or other forms of malicious input, the application uses SQLAlchemy's ORM to sanitize and validate database queries.