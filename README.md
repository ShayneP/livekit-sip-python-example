# Voice Assistant Agent with SIP Integration

This Python script implements a voice assistant using the LiveKit platform, with the ability to integrate with SIP trunks for phone call bridging.

## Features

- Voice Activity Detection (VAD) using Silero
- Speech-to-Text (STT) using OpenAI
- Language Model (LLM) using OpenAI
- Text-to-Speech (TTS) using OpenAI
- SIP trunk integration for phone call bridging

## Usage

The script sets up a voice assistant that:

1. Connects to a LiveKit room with audio-only subscription
2. Initializes the assistant with the necessary components
3. Starts the assistant in the connected room
4. Greets the user with a welcome message

To run the script, ensure you have the required dependencies installed and execute both:

`python agent.py dev`
`python call_phone.py`

Visit `http:/127.0.0.1:5001`, enter a phone number and call your agent.

## SIP Trunk Integration

To bridge phone calls to LiveKit rooms using SIP trunks, follow these steps:

1. Prerequisites:
   - Phone number from a SIP Trunk provider (e.g., Twilio or Telnyx)
   - LiveKit Cloud project or self-hosted LiveKit server
   - LiveKit CLI

2. Prepare SIP server:
   - For LiveKit Cloud, use the provided SIP server URI
   - For self-hosted, configure your SIP server

3. Create a SIP Trunk with your provider (e.g., Twilio or Telnyx)

4. Configure LiveKit CLI with your project details

5. Set up Outgoing Calls:
   - Add an Outbound Trunk

7. Test your setup:
   - Make incoming calls to your configured number
   - Use LiveKit CLI to initiate outgoing calls

For detailed instructions on each step, refer to the [LiveKit documentation on SIP integration](https://docs.livekit.io/sip/quickstart/).

> Note: Make sure to set up the necessary environment variables and API keys for the LiveKit platform, OpenAI services, and your SIP trunk provider before running the script and integrating with SIP!