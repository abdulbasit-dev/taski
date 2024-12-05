### Updated README File: **Tasky: PHP Task Manager with Authentication (Using PDO and MySQL)**

---

#### **Objective**

Build a secure and user-friendly PHP-based Task Manager application with MySQL as the database. The application will allow authenticated
users to manage their own tasks, including adding, editing, deleting, and searching tasks. The design will use Bootstrap for responsive and
modern styling.

---

### **Requirements**

#### **Authentication**

1. **User Registration**:

   - Allow new users to register using a registration form.
   - Validate username uniqueness and enforce password security (e.g., minimum 8 characters).
   - Store passwords securely using `password_hash()`.

2. **Login**:

   - Authenticate users with a login form.
   - Use PDO to validate credentials against the database, checking the hashed password.
   - Maintain session states for logged-in users.

3. **Logout**:

   - Provide a logout option to end the session and redirect to the login page.

4. **Restrict Access**:
   - Ensure that only authenticated users can access the task manager.
   - Redirect unauthorized users to the login page.

---

#### **Task Management**

1. **Task Dashboard**:

   - Display tasks belonging to the logged-in user in a table.
   - Columns: Task Name, Description, Status (Pending/Completed), Creation Date, Actions (Edit/Delete).

2. **Add Task**:

   - Provide a form to add new tasks.
   - Fields: Task Name, Description, and Status (default to Pending).
   - Validate form inputs before saving tasks.

3. **Edit Task**:

   - Allow users to update their own tasks, including changing details and status.
   - Prevent users from editing tasks belonging to other users.

4. **Delete Task**:

   - Allow users to delete their own tasks.
   - Prevent users from deleting tasks belonging to others.

5. **Search Tasks**:

   - Include a search bar to filter tasks by name or status.

---

#### **Additional Features**

1. **Ownership Restrictions**:

   - Ensure users can only access, edit, or delete tasks associated with their own account.

2. **Enhanced Validation**:

   - Add server-side validation to ensure data integrity.

3. **Confirmation Dialogs**:

   - Use Bootstrap modals to confirm actions like deleting a task.

4. **Task Completion Tracker**:

   - Show a progress indicator on the dashboard for completed vs. total tasks.

5. **User-Friendly Notifications**:
   - Use Bootstrap alerts to display messages for successful or failed operations (e.g., "Task added successfully!").

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

- Use **Bootstrap** for layout and design.
- Add a navigation bar with links to the dashboard, logout, and a welcome message for the logged-in user.
- Use Bootstrap cards, modals, and alerts to enhance user experience.

---

#### **Steps to Complete the Task**

1. **Setup**:

   - Install a local server environment like XAMPP or WAMP.
   - Create a MySQL database and tables (`users`, `tasks`).

2. **User Authentication**:

   - Create registration and login forms.
   - Use PDO prepared statements for secure database queries.
   - Implement session-based access control.

3. **Task Management**:

   - Implement CRUD functionality (Create, Read, Update, Delete) for tasks.
   - Restrict users to managing their own tasks.

4. **UI Design**:

   - Use Bootstrap components for the interface, including tables, buttons, modals, and alerts.

5. **Validation and Security**:

   - Validate form inputs.
   - Hash passwords and use prepared statements to prevent SQL injection.

---

#### **Deliverables**

1. A fully functional PHP application that:

   - Allows user registration and login.
   - Restricts task management to authenticated users.
   - Ensures users can only manage their own tasks.
   - Has a responsive and polished interface.

2. A MySQL script to create and populate the required tables.

3. Detailed documentation on installation and usage.

---

#### **Suggestions for Future Enhancements**

1. **Task Categories**:

   - Add support for categorizing tasks (e.g., Work, Personal).

2. **Deadline Management**:

   - Include a deadline field for tasks and highlight overdue tasks.

3. **Forgot Password Feature**:

   - Implement a password reset functionality via email.

---

#### **Evaluation Criteria**

1. Proper use of PDO and prepared statements for database interactions.
2. Secure authentication with password hashing.
3. Implementation of ownership restrictions to ensure data security.
