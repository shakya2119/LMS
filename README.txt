
Library Management System (LMS)

This project is a Library Management System (LMS) built using Flask and MySQL. It allows users to manage books, authors, publishers, racks, and users, along with providing functionalities like issuing and returning books. The project implements user authentication and authorization, ensuring secure access to its features.

Features
- User Authentication: Login, registration, password management.
- Book Management: Add, update, delete, view available, issued, and returned books.
- User Management: Add, update, delete, view users.
- Category, Author, Publisher, and Rack Management: Manage library categories, authors, publishers, and racks.
- Book Issuance: Issue and return books.
- Role-based Access Control: Differentiate features based on user roles.
  
Installation and Setup

Prerequisites
1. Python 3.x installed on your system.
2. MySQL database setup with the name LMS.
3. Required Python libraries installed (Flask, Flask-MySQLdb, MySQLdb).

Installation Steps
1. Clone or download this repository.
2. Create a virtual environment:
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
3. Install the required dependencies:
   pip install -r requirements.txt
4. Configure the database:
   - Create a MySQL database named LMS.
   - Update the app.config variables in app.py with your MySQL host, username, and password.

5. Run the application:
   python app.py

6. Access the application in your web browser at http://localhost:5000.

Design Choices
1. Framework: Flask was chosen for its lightweight nature and ease of implementation.
2. Database: MySQL is used for its reliability and integration with Flask.
3. Session Management: Flask sessions ensure that user data persists during a session.
4. Templating Engine: Jinja2 is used to render dynamic HTML content.
5. Role-based Access Control: Only logged-in users can access features, and specific actions may depend on roles.

Assumptions and Limitations

Assumptions
- All users will have unique email addresses for login.
- The database schema is pre-configured and contains all required tables (e.g., user, book, author, etc.).

Limitations
- Limited error handling for database operations.
- Passwords are stored in plain text, which is insecure. It is recommended to implement hashing.
- No automated tests are included.
- Email validation uses a simple regex and might not cover all valid email formats.
- Designed for local development; additional security measures are required for production.

Future Improvements
- Add hashed passwords using libraries like bcrypt.
- Implement detailed logging for debugging.
- Add role-based feature restrictions directly in routes.
- Extend functionalities with RESTful APIs for easier integration with other systems.
- Introduce unit and integration tests.

Feel free to expand on this documentation as the project evolves.
