# Speech Models

This folder contains the Docker-based IBM Watson speech services used by the voice chat application in this repo.

## Included services

- [stt](stt) – Speech-to-Text model container
- [tts](tts) – Text-to-Speech model container

## Project role

These model services are used to support the voice assistant app by enabling:

- speech recognition from user audio input
- speech synthesis for AI responses

## Notes

These containers are based on IBM Watson Speech services and require the proper IBM entitlement configuration before they can be built or run locally.

## Typical workflow

1. Build and start the STT container.
2. Build and start the TTS container.
3. Connect the application server to these local endpoints.
4. Use the voice assistant app for real-time interaction.

## Useful references

- [stt/README.md](stt/README.md)
- [tts/README.md](tts/README.md)
