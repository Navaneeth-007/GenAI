# STT Model Container

This folder contains the IBM Watson Speech-to-Text container used by the voice-based GenAI project in this repository.

## Purpose

The STT service is used to convert spoken audio into text so the main application can process user voice input and send it to the AI model.

## Files in this folder

- [Dockerfile](Dockerfile) – build instructions for the speech-to-text container
- [prepareModels.sh](prepareModels.sh) – model preparation script
- [chuck_var](chuck_var) – model and service configuration files

## Typical build command

```bash
docker build . -t stt-standalone
```

## Typical run command

```bash
docker run --rm -it --env ACCEPT_LICENSE=true --publish 1080:1080 stt-standalone
```

## Usage in this project

This STT service is connected to the main voice app in the parent project. The app sends recorded audio to the local Speech-to-Text endpoint and then uses the extracted text in the conversational flow.

## Notes

- This requires IBM entitlement access for the Watson speech containers.
- The service is best used together with the matching TTS container from the sibling folder.
