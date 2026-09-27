# JARVIS

Personal room assistant project inspired by JARVIS.

JARVIS is being built as a modular system around Home Assistant, with Gemini providing the conversational AI layer and Home Assistant handling devices and automations.

## Current status

- Home Assistant OS running in VirtualBox on Windows 11
- Home Assistant reachable locally
- Gemini configured as the conversation agent
- Voice input working from the browser
- Google Translate TTS working
- Piper installed as a local TTS fallback
- WiZ integrated
- Smart Life / Tuya integrated
- Room network consolidated through the Deco E4 in Access Point mode

## Architecture

```
Voice input
    |
    v
Home Assistant Assist
    |
    v
Gemini conversation agent
    |
    v
Home Assistant
   / \
  /   \
WiZ   Smart Life / Tuya

TTS -> Google Translate
      Piper (fallback)
```

## Repository structure

- `home-assistant/` - safe, portable Home Assistant configuration templates and notes
- `integrations/` - integration-specific documentation
- `voice/` - voice assistant and TTS documentation
- `webapp/` - future JARVIS web application
- `docs/` - architecture, deployment, networking and roadmap
- `scripts/` - future helper scripts

## Security

Never commit:

- API keys
- passwords
- access tokens
- Home Assistant secrets
- private device credentials
- private IP/device data that should not be public

Use placeholders and environment variables instead.

## Roadmap

1. Stabilize Home Assistant device control
2. Improve voice latency and TTS quality
3. Add wake-word activation ("JARVIS")
4. Add webcam vision
5. Build the JARVIS web app
6. Connect the web app to a secure Home Assistant API layer
7. Add ESP32/sensors and room hardware
