# Architecture

## Current

Home Assistant is the local orchestration layer.

Gemini is the conversational intelligence layer.

WiZ and Smart Life/Tuya provide smart-light control.

The system currently runs locally on a Windows 11 PC with Home Assistant OS in VirtualBox.

## Future web app

The future web application should not expose Home Assistant credentials directly to the browser.

Target:

Browser
  |
  v
JARVIS Web App
  |
  v
Secure backend/API layer
  |
  v
Home Assistant

The backend should handle authentication, secrets and Home Assistant API access.
