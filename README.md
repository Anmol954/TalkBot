# 🎙️🤖 Voice ChatBot with OpenAI

A voice-enabled chatbot application built with Streamlit that allows users to interact with OpenAI's GPT models using voice input and receive spoken responses.

## ✨ Features

- 🎤 **Voice Recording**: Record your questions directly in the browser
- 🔊 **Speech-to-Text**: Converts your voice input to text using OpenAI's Whisper model
- 💬 **AI Responses**: Generates intelligent responses using GPT-3.5-turbo
- 🗣️ **Text-to-Speech**: Converts AI responses back to audio using OpenAI's TTS model
- 🖥️ **User-Friendly Interface**: Simple and intuitive Streamlit web interface

## 🛠️ Technologies Used

- **Streamlit**: Web application framework
- **OpenAI API**: 
  - Whisper (speech-to-text)
  - GPT-3.5-turbo (chat completion)
  - TTS-1 (text-to-speech)
- **Python**: Backend programming language
- **audio-recorder-streamlit**: Audio recording component

## 📋 Prerequisites

- Python 3.7 or higher
- OpenAI API key

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Voicechatbot-openai-main
   ```

2. **Install required packages**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the project root directory and add your OpenAI API key:
   ```
   OPENAI_API_KEY=your_openai_api_key_here
   ```

## 💻 Usage

1. **Run the application**
   ```bash
   streamlit run app.py
   ```

2. **Interact with the chatbot**
   - Click the "Click to record" button to start recording your voice
   - Speak your question or message
   - Click again to stop recording
   - Click the "🎙️Get Response🎙️" button to get the AI's response
   - Listen to the audio response and view the text transcription

## 📁 Project Structure

```
Voicechatbot-openai-main/
│
├── app.py                  # Main Streamlit application
├── chatbot_function.py     # Core chatbot functions (speech-to-text, text-to-speech, chat)
├── requirements.txt        # Python dependencies
├── .env                    # Environment variables (create this file)
└── README.md              # Project documentation
```

## 🔧 Configuration

### Voice Selection
You can change the TTS voice in `chatbot_function.py`. Available voices include:
- `alloy`
- `echo`
- `fable` (current)
- `onyx`
- `nova`
- `shimmer`

Modify line in the `text_to_speech_conversion` function:
```python
voice="fable"  # Change to your preferred voice
```

### AI Model
To use a different GPT model, modify the model parameter in `chatbot_function.py`:
```python
model="gpt-3.5-turbo"  # Change to gpt-4, gpt-4-turbo, etc.
```

## 🔐 API Key Security

- Never commit your `.env` file to version control
- Add `.env` to your `.gitignore` file
- Keep your OpenAI API key confidential

## 📝 How It Works

1. **Audio Recording**: User records audio through the browser using the audio recorder component
2. **Speech-to-Text**: The audio is sent to OpenAI's Whisper model for transcription
3. **Chat Processing**: The transcribed text is sent to GPT-3.5-turbo for generating a response
4. **Text-to-Speech**: The AI's text response is converted to audio using OpenAI's TTS model
5. **Output**: Both text and audio responses are displayed to the user

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## ⚠️ Troubleshooting

### Common Issues

1. **API Key Error**
   - Ensure your `.env` file is in the project root
   - Verify your OpenAI API key is valid and has sufficient credits

2. **Audio Recording Issues**
   - Make sure your browser has microphone permissions enabled
   - Try using Chrome or Firefox for best compatibility

3. **Installation Issues**
   - Ensure you have Python 3.7+ installed
   - Try upgrading pip: `pip install --upgrade pip`

## 📧 Support

For issues, questions, or suggestions, please open an issue in the repository.

## 🙏 Acknowledgments

- OpenAI for providing the API services
- Streamlit for the web framework
- The audio-recorder-streamlit library contributors

---

**Note**: This application requires an active OpenAI API key and will incur costs based on usage. Please refer to [OpenAI's pricing page](https://openai.com/pricing) for current rates.
