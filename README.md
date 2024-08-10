
# Capstone To-Do List Project

This project is a simple To-Do List web application built using Node.js, Express, PostgreSQL, and EJS templating. The application allows users to add, edit, and delete tasks from their to-do list, which is stored in a PostgreSQL database.

## Features

- **View To-Do List:** Displays all tasks stored in the PostgreSQL database.
- **Add Tasks:** Users can add new tasks to their to-do list.
- **Edit Tasks:** Users can edit the title of existing tasks.
- **Delete Tasks:** Users can delete tasks from their to-do list.
- **Responsive Design:** The application is designed to work well on different screen sizes.

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/RUBBOSS/capstone-todo-list.git
    cd capstone-todo-list
    ```

2. Install the necessary dependencies:

    ```bash
    npm install
    ```

3. Set up the PostgreSQL database:

    - Make sure you have PostgreSQL installed and running.
    - Create a database named `permalist`.
    - Use the following credentials to connect to the database (or modify the code in `index.js` to match your setup):

      ```json
      {
        "user": "postgres",
        "host": "localhost",
        "database": "permalist",
        "password": "yourpassword",
        "port": 5432
      }
      ```

    - Create a table for storing the to-do list items:

      ```sql
      CREATE TABLE items (
          id SERIAL PRIMARY KEY,
          title VARCHAR(255) NOT NULL
      );
      ```

4. Start the application:

    ```bash
    npm start
    ```

5. Open your browser and navigate to `http://localhost:3000` to see the application in action.

## Project Structure

- `index.js`: Main server file where Express is configured and routes are defined.
- `views/`: Contains the EJS templates for rendering HTML.
- `public/`: Contains static assets such as CSS and images.
- `package.json`: Contains the project dependencies and scripts.

## Usage

- **Add a new task:** Use the input field at the bottom of the list to add a new task. Press the `+` button or hit `Enter` to submit.
- **Edit a task:** Click the pencil icon next to a task to edit its title. Press the checkmark to save the changes.
- **Delete a task:** Check the checkbox next to a task to delete it.

