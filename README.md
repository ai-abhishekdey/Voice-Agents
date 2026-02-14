##  Clinical Voice Assistant with End-to-End Speech Intelligence

**Author: Abhishek Dey**

## Problem Statement:

To build a real-time voice agent in English Language who is checking with a patient, regarding the post surgery followup.   Patient had Ankle surgery after a fall from a horse while playing Polo and is enrolled into a home program for recovery.

- Agent has to perform the following checkin related questions (a to e questions) in sequential manner:
  - a. Introduce yourself about why you called the patient.
  - b. Ask about how the patient is feeling after surgery
  - c. Assess the pain score (1-10)
  - d. Guide the patient to work on the following exercises one by one (to have faster recovery):
     - Ankle Mobility Stretch
     - Toe Tapping
     -  Calf Raises.
     - After explaining instructions to do the above exercises, ask: “Would you like to take a moment to go through the steps for [exercise name] now? and tell
that you can hold/pause the call upto one minute.
  - e. Call closing

## Voice Agent Development:

The voice agent is developed using **pipecat** framework considering the following AI Model services

1. **Deepgram** for ASR
2. **Cartesia** for TTS
3. **OpenAI** for LLM
4. **Silero-vad** for Voice  Activity Detection

## Getting Started:
---
## Get API Keys:

1. Get Deepgram API from [here](https://console.deepgram.com/signup)
2. Get OpenAI API Key from [here](https://auth.openai.com/create-account)
3. Get Cartesia API Key from [here](https://play.cartesia.ai/sign-up)

## Configure your API keys

* Copy the sample environment file as .env

```
cp env.example .env
```

* Open the .env file in your text editor and add your API keys:

```
DEEPGRAM_API_KEY=your_deepgram_api_key
OPENAI_API_KEY=your_openai_api_key
CARTESIA_API_KEY=your_cartesia_api_key
```

## Set up virtual environment and install dependencies

```
uv sync

```

## Run your bot locally

```
uv run bot.py
```

* You should see output similar to this:

```
🚀 Bot ready!
   → Open http://localhost:7860/client in your browser

INFO:     Started server process [55397]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
INFO:     Uvicorn running on http://localhost:7860 (Press CTRL+C to quit)
```
## Note: 

* To check the process using port: 7860

```
lsof -i :7860
```

* To kill the process

```
kill -9 <PID>
```

## Demo:

- [Click here for the demo](https://drive.google.com/file/d/1dRB-VmMniLspnN3QVPFz8fXoc-aZp2yJ/view?usp=drive_link)


## References:

1. [Pipecat Documentation](https://docs.pipecat.ai/getting-started/introduction)
2. [Pipecat QuickStart](https://github.com/pipecat-ai/pipecat-quickstart)
3. [Cartesia](https://cartesia.ai/sonic)
4. [Deepgram](https://developers.deepgram.com/docs/pre-recorded-audio)
5. [OpenAI](https://openai.com/)
6. [Silero-vad](https://github.com/snakers4/silero-vad)

