# Audio Analyzer

This folder contains experiments focused on audio processing and speech intelligence using Hugging Face models and IBM Watson-based AI workflows.

## Project purpose

The scripts in this folder demonstrate how to:

- transcribe audio using Whisper
- analyze speech content using an LLM
- combine speech recognition with text generation
- create simple Gradio web interfaces for audio-based tasks

## Files in this folder

- [hello.py](hello.py) – basic starter script for initial testing and experimentation.
- [simple_llm.py](simple_llm.py) – a simple example using a language model through IBM Watson AI infrastructure.
- [simple_speech2text.py](simple_speech2text.py) – basic speech-to-text conversion with Whisper.
- [speech2text_app.py](speech2text_app.py) – Gradio app for uploading audio and transcribing it.
- [speech_analyzer.py](speech_analyzer.py) – more advanced workflow that combines speech transcription with LLM-based summarization and analysis.

## Technologies used

- Python
- PyTorch
- Hugging Face Transformers
- OpenAI Whisper
- Gradio
- IBM watsonx / IBM Watson Machine Learning

## Typical workflow

1. Upload or select an audio file.
2. Convert speech to text using Whisper.
3. Pass the transcript to a language model for analysis or summarization.
4. Display the result in the interface or terminal.

## Example usage

```bash
python speech2text_app.py
```

Then open the Gradio interface in the browser and upload an audio file.

## Learning outcome

This project helped practice the integration of speech models, transformers, and LLMs into a single AI workflow for audio understanding.
