# PropBot - Real Estate AI Assistant

PropBot is an AI-powered real estate assistant that helps users with property-related queries, including buying, selling, renting, investing, and understanding the market. The application is built using Flask for the backend, Google Gemini for AI responses, and a modern HTML/CSS/JavaScript frontend.

## Features

- **Real Estate Expertise**: PropBot can answer questions related to buying, selling, renting, investing, and market trends.
- **Markdown Support**: Users can format their messages using Markdown for better readability.
- **Conversation History**: The chatbot maintains a conversation history for the current session.
- **Responsive Design**: The chatbot interface is fully responsive and works on both desktop and mobile devices.
- **Quick Suggestions**: Users can click on quick suggestion chips to ask common real estate questions.

## Technologies Used

- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Flask (Python)
- **AI**: Google Gemini API
- **Markdown Parsing**: `marked.js`
- **Styling**: Animate.css, Font Awesome, Google Fonts

## Prerequisites

Before running the application, ensure you have the following installed:

- Python 3.x
- Flask
- Google Gemini API key (stored in `.env` file)

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/PropBot.git
   cd PropBot
   ```

2. **Set up a virtual environment** (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up the `.env` file**:
   Create a `.env` file in the root directory and add your Google Gemini API key:
   ```plaintext
   GEMINI_API_KEY=your_api_key_here
   SECRET_KEY=your_secret_key_here
   ```

## Running the Application

To run the application on port 5000, use the following command:

```bash
python app.py
```

The application will be available at `http://localhost:5000`.

## API Endpoints

- **GET `/`**: Serves the main chatbot interface.
- **POST `/chat`**: Handles user messages and returns AI responses.
- **GET `/history`**: Returns the conversation history for the current session.
- **POST `/clear_history`**: Clears the conversation history for the current session.

## Deployment

To deploy the application to a production environment, you can use services like:

- **Heroku**
- **AWS Elastic Beanstalk**
- **Google Cloud Run**
- **Docker** (containerize the app and deploy to any container orchestration platform)

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

### Running on Port 5000

The application is configured to run on port 5000 by default. If you want to change the port, you can modify the `app.run()` line in `app.py`:

```python
if __name__ == '__main__':
    app.run(debug=True, port=5000)  # Change the port number if needed
```

To run the app, simply execute:

```bash
python app.py
```

The app will start, and you can access it at `http://localhost:5000`.

---

### Notes

- Ensure that the `.env` file is not committed to the repository (it’s already included in `.gitignore`).
- The app uses Flask’s built-in development server, which is suitable for development but not for production. For production, consider using a WSGI server like Gunicorn or deploying via Docker.

---

This `README.md` provides a comprehensive guide for setting up, running, and deploying the PropBot application. You can now push this project to your GitHub repository!
