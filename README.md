# Employee_Info: Chat with SQLite DB

## Overview
This is a Streamlit-based chatbot that allows users to interact with an SQLite database using natural language queries. It leverages LangChain and OpenAI's GPT-4 model to interpret and execute SQL queries against the database, providing meaningful responses.

## Features
- **Natural Language to SQL**: Converts user queries into SQL and retrieves relevant information from the database.
- **Streamlit UI**: Provides an interactive chat interface for seamless user experience.
- **Persistent Chat History**: Maintains message history for context-aware interactions.
- **Error Handling**: Detects invalid queries and returns meaningful error messages.
- **Secure API Key Management**: Uses Streamlit secrets to handle the OpenAI API key securely.

## Requirements
- Python 3.8+
- Streamlit
- LangChain
- OpenAI API key
- SQLite3
- SQLAlchemy

## Installation
1. Clone the repository:
   ```sh
   git clone <repo_url>
   cd <repo_folder>
   ```
2. Create a virtual environment and activate it:
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```

## Setup
1. Place your `company.db` SQLite database file in the project directory.
2. Store your OpenAI API key securely in Streamlit secrets:
   ```sh
   mkdir -p ~/.streamlit
   echo "[secrets]\nOPENAI_API_KEY='your_api_key_here'" > ~/.streamlit/secrets.toml
   ```

## Running the Application
Run the Streamlit app with the following command:
```sh
streamlit run app.py
```

## Usage
1. Start the application and enter your query in natural language.
2. The chatbot processes the query and fetches results from the SQLite database.
3. If the query is invalid or unrelated, it provides a meaningful error message.

## Error Handling
- If the query is not related to the database, it returns: _"The query seems to be unrelated to the database, Please recheck."_
- If any execution error occurs, it returns an appropriate error message to guide the user.

## Future Enhancements
- Support for multiple database connections.
- Enhanced NLP capabilities for better query interpretation.
- Integration with other LLM models for improved accuracy.

## License
This project is open-source and available under the [MIT License](LICENSE).


