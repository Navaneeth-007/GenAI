# Image Captioning

This folder contains a simple image captioning application built with a pre-trained Vision-Language model from Hugging Face.

## Project purpose

The project demonstrates how to:

- load a pre-trained BLIP model
- process uploaded images
- generate descriptive captions
- build a Gradio application for image input and output

## Files in this folder

- [image_captioning_app.py](image_captioning_app.py) – main image captioning app using BLIP.
- [automate_url_captioner.py](automate_url_captioner.py) – helper script for captioning images from URLs or automated sources.
- [myapp](myapp) – a small sub-project for a simple demo app setup.

## Technologies used

- Python
- PyTorch
- Hugging Face Transformers
- PIL (Python Imaging Library)
- Gradio
- Salesforce BLIP model

## How it works

1. The user uploads or provides an image.
2. The image is converted to a format suitable for the model.
3. The BLIP processor prepares the image.
4. The model generates a natural-language caption.
5. The caption is displayed in the UI.

## Run it

```bash
python image_captioning_app.py
```

or use the demo app inside the [myapp](myapp) folder if needed.

## Learning outcome

This project introduced the basics of vision-language models and how they can be used for real-world image understanding tasks.
