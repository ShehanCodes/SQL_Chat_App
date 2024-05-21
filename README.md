# Chat with MySQL

## Description

This is a simple chat application built with Streamlit that allows users to interact with a MySQL database using natural language queries. The application leverages language models to translate user queries into SQL commands, executes them against the database, and returns the results in a conversational format.

## Features

- Connect to a MySQL database.
- Ask natural language questions about the database.
- Receive SQL query results in a conversational format.
- Maintain chat history during the session.

## Requirements

- Python 3.7 or higher
- Streamlit
- Langchain libraries
- MySQL database
- .env file for environment variables (optional)

## Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/yourusername/chat-with-mysql.git
    ```

2. Navigate to the project directory:

    ```sh
    cd chat-with-mysql
    ```

3. Install the required dependencies:

    ```sh
    pip install -r requirements.txt
    ```

4. (Optional) Create a `.env` file to store your environment variables:

    ```sh
    touch .env
    ```

    Add your environment variables in the following format:

    ```env
    HOST=localhost
    PORT=3306
    USER=root
    PASSWORD=admin
    DATABASE=Chinook
    ```

## Usage

1. Run the Streamlit application:

    ```sh
    streamlit run app.py
    ```

2. Open your web browser and go to `http://localhost:8501` to view the application.

3. In the sidebar, enter your database connection details (Host, Port, User, Password, Database) and click "Connect".

4. Once connected, type your query in the chat input box and press Enter. The application will respond with the SQL query result.

## Code Overview

### Functions

- **init_database**: Initializes the connection to the MySQL database using the provided credentials.
- **get_sql_chain**: Generates the SQL query from the user’s natural language input.
- **get_response**: Executes the SQL query against the database and formats the response in natural language.

### Main Workflow

1. The application starts by loading environment variables and setting up the Streamlit interface.
2. Users enter their database connection details in the sidebar.
3. Upon connection, users can type natural language queries in the chat input box.
4. The application translates the query into SQL, executes it, and returns the result in a conversational format.
5. The chat history is maintained throughout the session.

## Customization

- The language model and parameters can be adjusted in the `get_sql_chain` and `get_response` functions to use different models or settings.

