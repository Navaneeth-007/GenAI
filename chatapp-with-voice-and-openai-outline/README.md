# Voice Chat Assistant

This project is a voice-enabled AI assistant built as part of the IBM GenAI learning course. It combines speech recognition, speech synthesis, and generative AI responses into a simple web app experience.

## Project purpose

The application demonstrates how to:

- convert spoken audio to text using a speech-to-text service
- send the transcribed text to an AI model for response generation
- convert the generated text back to speech
- build a Flask-based app that connects voice input and output

## Main files

- [server.py](server.py) – Flask server with API endpoints for chat and audio processing
- [worker.py](worker.py) – logic for speech-to-text, text-to-speech, and OpenAI API integration
- [templates/index.html](templates/index.html) – interface for the web app
- [static/script.js](static/script.js) – frontend logic for interacting with the app
- [static/style.css](static/style.css) – styles for the interface
- [models](models) – containerized Watson speech model resources for STT/TTS

## Technologies used

- Python
- Flask
- requests
- OpenAI API
- IBM Watson Speech-to-Text
- IBM Watson Text-to-Speech

## Workflow

1. User speaks or uploads audio.
2. The backend calls the speech-to-text API.
3. The recognized text is passed to a language model.
4. The AI response is converted to speech.
5. The frontend returns both text and audio output to the user.

## Run locally

```bash
pip install -r requirements.txt
python server.py
```

Then open the app in the browser and start interacting with the assistant.

## Learning outcome

This project helped practice full-stack voice app design, API integration, and the combination of speech pipelines with generative AI.
