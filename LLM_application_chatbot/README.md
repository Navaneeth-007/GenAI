# LLM Application Chatbot

This folder contains a Flask-based chatbot web application that uses a transformer language model to generate responses to user messages.

## Project purpose

This project demonstrates how to:

- build a simple web app with Flask
- connect a frontend form to a local language model
- generate responses using a pre-trained seq2seq model
- serve the app through a browser UI

## Main file

- [app.py](app.py) – Flask server and chatbot logic.

The app also uses:

- [static/script.js](static/script.js) – frontend interaction logic
- [static/css/style.css](static/css/style.css) – UI styling
- [templates/index.html](templates/index.html) – HTML interface

## Technologies used

- Python
- Flask
- Flask-CORS
- Hugging Face Transformers
- PyTorch
- BlenderBot model

## Workflow

1. The user enters a prompt in the browser.
2. The Flask server receives the request.
3. The model generates a response.
4. The response is returned to the frontend and displayed to the user.

## Run it

```bash
pip install -r requirements.txt
python app.py
```

Then open the local URL shown in the terminal.

## Learning outcome

This project is a practical introduction to creating a simple LLM-powered web application, combining backend AI logic with a browser-based user interface.
