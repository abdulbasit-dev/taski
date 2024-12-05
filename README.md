### PHP Task Assignment: Task Manager with Authentication (Using PDO and MySQL)

---

#### **Objective**

Build a PHP-based Task Manager with authentication using MySQL as the database. The application will allow users to manage their tasks,
including adding, editing, deleting, and searching tasks. The design will use Bootstrap for styling.

---

### **Requirements**

#### **Authentication**

1. **User Registration**:

   - Create a registration form to allow new users to sign up.
   - Validate that the username is unique and the password meets security criteria (e.g., minimum 8 characters).
   - Hash passwords using `password_hash()` before saving them to the database.

2. **Login**:

   - Create a login page to authenticate users.
   - Use PDO to query the database and validate the username and hashed password.
   - Use sessions to maintain the user's login status.

3. **Logout**:

   - Provide a logout button to end the session and redirect to the login page.

4. **Restrict Access**:
   - Only logged-in users should have access to the task manager dashboard.

---

#### **Task Management**

1. **Task Dashboard**:

   - Display tasks for the logged-in user in a table.
   - Columns: Task Name, Description, Status (Pending/Completed), Creation Date, Actions (Edit/Delete).

2. **Add Task**:

   - Provide a form to add new tasks.
   - Fields: Task Name, Description, and Status (default to Pending).
   - Validate the form input.

3. **Edit Task**:

   - Allow users to update a task's details and status.

4. **Delete Task**:

   - Allow users to delete tasks.

5. **Search Tasks**:
   - Add a search bar to filter tasks by name or status.

---

#### **Database Structure**

Create a MySQL database with the following tables:

1. **`users`**:

   - `id` (Primary Key, Auto Increment)
   - `username` (VARCHAR, Unique)
   - `password` (VARCHAR)

2. **`tasks`**:
   - `id` (Primary Key, Auto Increment)
   - `user_id` (Foreign Key to `users.id`)
   - `name` (VARCHAR)
   - `description` (TEXT)
   - `status` (ENUM: 'Pending', 'Completed')
   - `created_at` (TIMESTAMP)

---

#### **Styling**

- Use Bootstrap for layout and design.
- Implement a responsive design for the task manager interface.
- Include a navigation bar with links to the dashboard, logout, and a welcome message for the logged-in user.

---

#### **Steps to Complete the Task**

1. **Setup**:

   - Install a local server environment like XAMPP or WAMP.
   - Create a MySQL database and tables (`users`, `tasks`).

2. **User Authentication**:

   - Create forms for registration and login.
   - Use PDO to interact with the database for user validation.
   - Use sessions to manage login states.

3. **Task Management**:

   - Build CRUD functionality (Create, Read, Update, Delete) for tasks.
   - Filter tasks by the logged-in user's `user_id`.

4. **UI Design**:

   - Use Bootstrap components (tables, forms, buttons, modals) for the interface.

5. **Validation and Security**:

   - Validate all form inputs.
   - Use prepared statements with PDO to prevent SQL injection.
   - Hash passwords for secure storage.

6. **Test**:
   - Test the application for different scenarios, including login/logout, adding tasks, and editing/deleting tasks.

---

#### **Deliverables**

1. A fully functional PHP application that:
   - Allows user registration and login.
   - Lets users manage their tasks.
   - Restricts access to authenticated users.
2. A MySQL script to create and populate the required tables.
3. A clean and responsive UI designed with Bootstrap.

---

#### **Evaluation Criteria**

1. Proper use of PDO for database interactions.
2. Secure authentication using password hashing.
3. Clean and maintainable PHP code with proper validation.
4. Responsive and user-friendly design.
5. Correct functionality for all features.
