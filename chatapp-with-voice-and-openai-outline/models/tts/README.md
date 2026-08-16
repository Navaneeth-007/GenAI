# TTS Model Container

This folder contains the IBM Watson Text-to-Speech container used by the voice assistant project.

## Purpose

The TTS service converts AI-generated text back into spoken audio so the chatbot can respond with voice output.

## Files in this folder

- [Dockerfile](Dockerfile) – container build instructions
- [prepareModels.sh](prepareModels.sh) – setup script for the required models
- [config](config) – service configuration files

## Typical build command

```bash
docker build . -t tts-standalone
```

## Typical run command

```bash
docker run --rm -it --env ACCEPT_LICENSE=true --publish 1081:1080 tts-standalone
```

## Usage in this project

The main voice app sends generated text to the TTS endpoint, which returns audio data. The app then plays or returns that audio in the front-end experience.

## Notes

- This service requires IBM Watson Speech container access.
- It is designed to work together with the STT service container in the sibling folder.

            "description": "Kate: British English female voice. Dnn technology.",
            "customizable": true,
            "supported_features": {
                "custom_pronunciation": true,
                "voice_transformation": false
            },
            "url": "http://localhost:1081/text-to-speech/api/v1/voices/en-GB_KateV3Voice"
        }
    ]
}
```

Generate an audio file in English.

```sh
curl "http://localhost:1081/text-to-speech/api/v1/synthesize" \
  --header "Content-Type: application/json" \
  --data '{"text":"Hello world"}' \
  --header "Accept: audio/wav" \
  --output output.wav
```

Then output will be in `output.wav`.

Next, try the French model.

```sh
curl "http://localhost:1081/text-to-speech/api/v1/synthesize?voice=fr-CA_LouiseV3Voice" \
  --header "Content-Type: application/json" \
  --data '{"text":"Bonjour le monde."}' \
  --header "Accept: audio/wav" \
  --output french-test.wav
```

The output will be in `french-test.wav`.

## Acknowledgements

This repository was created based off the [IBM Build Lab Watson Speech repository](https://github.com/ibm-build-lab/Watson-Speech). Specifically, their `single-container-tts` directory.