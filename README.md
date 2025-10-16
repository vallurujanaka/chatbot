# Bhavana's Personal Chatbot Assistant

A premium, sci-fi themed personal chatbot assistant built with Flask, HTML, CSS, and JavaScript. This AI-powered assistant uses OpenRouter API to provide personalized, helpful, and warm responses specifically tailored for Bhavana.

## Features

- **Personalized AI Assistant**: Custom system prompt designed specifically for Bhavana
- **Real-time Chat Interface**: Interactive web-based chat with typing indicators
- **Premium Design**: Gold and black sci-fi theme with glowing effects
- **Conversation History**: Maintains context throughout the chat session
- **Well-formatted Responses**: Assistant responses are properly indented and structured
- **Responsive Design**: Works on desktop and mobile devices
- **Flask Backend**: Robust Python backend with RESTful API endpoints

## Screenshots

![Chat Interface](https://via.placeholder.com/800x600/000000/FFD700?text=Bhavana%27s+Chatbot+Interface)

## Prerequisites

- Python 3.7 or higher
- Valid OpenRouter API key (sign up at [openrouter.ai](https://openrouter.ai))

## Installation

1. **Clone the repository** (if applicable) or ensure you have the project files:
   - `app.py`
   - `templates/index.html`
   - `main.py` (original CLI version)

2. **Install dependencies**:
   ```bash
   pip install flask openai
   ```

3. **Set up your API key**:
   - Replace the hardcoded API key in `app.py` with your own OpenRouter API key, or better yet, use environment variables for security:
     ```bash
     export OPENROUTER_API_KEY=your_api_key_here
     ```
     Then modify `app.py` to use `os.getenv("OPENROUTER_API_KEY")` instead of the hardcoded key.

## Usage

### Running the Web Application

1. **Start the Flask server**:
   ```bash
   python app.py
   ```

2. **Open your browser** and navigate to:
   ```
   http://127.0.0.1:5000
   ```

3. **Start chatting**: Type your messages in the input field and press Enter or click Send.

### CLI Version (main.py)

For a command-line interface version:
```bash
python main.py
```

Type your messages and press Enter. Type 'quit' to exit.

## Project Structure

```
bhavana-chatbot/
├── app.py                 # Flask application backend
├── main.py                # CLI version of the chatbot
├── templates/
│   └── index.html         # Web interface
└── README.md              # This file
```

## API Endpoints

- `GET /`: Serves the main chat interface
- `POST /chat`: Accepts JSON with 'message' field, returns AI response

Example API usage:
```bash
curl -X POST http://127.0.0.1:5000/chat \
  -H "Content-Type: application/json" \
  -d '{"message": "Hello, how are you?"}'
```

## Customization

### Changing the Theme
Edit the CSS in `templates/index.html` to modify colors, fonts, or layout.

### Modifying the AI Personality
Update the system message in `app.py`:
```python
messages = [
    {"role": "system", "content": "Your custom system prompt here"}
]
```

### Adding Features
- Voice input/output
- File upload capabilities
- User authentication
- Database integration for persistent chat history

## Technologies Used

- **Backend**: Python, Flask
- **Frontend**: HTML5, CSS3, JavaScript
- **AI**: OpenRouter API (NVIDIA Nemotron model)
- **Styling**: Custom CSS with sci-fi theme

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

If you encounter any issues or have questions:
- Check the Flask server logs for error messages
- Ensure your OpenRouter API key is valid and has sufficient credits
- Verify all dependencies are installed correctly

## Future Enhancements

- [ ] Voice input and output capabilities
- [ ] Dark/light theme toggle
- [ ] Export chat history
- [ ] Multi-language support
- [ ] Integration with other AI models
- [ ] User profile customization

---

