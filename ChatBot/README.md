# ChatBot

This folder contains small conversational AI experiments built with transformer-based chat models. The goal is to learn how to build a chatbot using pre-trained models and interactive terminal-based prompts.

## Project purpose

The scripts in this folder focus on:

- chat generation with conversational models
- context handling across multi-turn conversations
- prompt construction for interactive chat
- model inference with Hugging Face Transformers

## Files in this folder

- [chatbot.py](chatbot.py) – chatbot built using BlenderBot, a conversational model from Hugging Face.
- [chatbot_llm.py](chatbot_llm.py) – a second chatbot implementation using a smaller causal LM model for terminal-based chat.

## Technologies used

- Python
- PyTorch
- Hugging Face Transformers
- AutoTokenizer
- AutoModelForSeq2SeqLM
- AutoModelForCausalLM

## How it works

The bot reads user input, keeps a recent history of the conversation, converts the text into tokens, sends it to the model, and then generates a response. This allows a simple chat loop that resembles a conversational assistant.

## Example usage

```bash
python chatbot.py
```

or

```bash
python chatbot_llm.py
```

Then type messages in the terminal and use `exit` to quit.

## Learning outcome

This project helped with understanding conversational model usage, tokenization, generation parameters, and rule-based chat flow control in Python.
