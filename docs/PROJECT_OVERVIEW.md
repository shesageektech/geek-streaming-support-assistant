# Project Overview

## Purpose and audience

GEEK Streaming Support Assistant turns common streaming-device troubleshooting into a guided conversation. It identifies the user’s issue, recommends a relevant first-line action, and checks whether the action worked.

The experience is designed for everyday users who may not feel confident troubleshooting hardware, network, audio/video, or remote-control problems on their own. It uses plain language, short prompts, and button-based choices.

## Troubleshooting coverage

| Category | Symptom | Diagnostic focus |
|---|---|---|
| Power | Device will not turn on | Status light, TV input, HDMI, and power cable |
| Power | Device keeps restarting | USB power, wall adapter, and power cycle |
| Connection | No internet | Other-device connectivity, router restart, and network reconnection |
| Connection | Buffering | Device placement, signal obstruction, quality settings, and restart |
| Audio/Video | Blank or black screen | HDMI cable, port, and TV input |
| Audio/Video | No sound | Mute, volume, and audio-output settings |
| Remote | Unresponsive remote | Batteries, residual power, and pairing |
| Remote | Voice features | Internet connection, account sign-in, and re-pairing |

## Core conversation structure

1. Greeting and purpose
2. Main-menu category
3. Symptom selection
4. Diagnostic question
5. Targeted troubleshooting step
6. Resolution check
7. Success or escalation preparation
8. More-help navigation or final closing

## Product boundary

The original Python logic uses ticket-creation messages to represent intended future escalation. The current Landbot build does not create a ticket or transfer to a live agent.

Its current endpoint is to collect the user’s details, save the form fields, and show a personalized confirmation. External ticket creation and live handoff are future-version ideas.

## Future opportunities

- Connect the escalation form to an automation platform
- Send support requests to email, Google Sheets, or a ticketing system
- Generate a ticket number and status confirmation
- Add a live-agent or Tier 2 handoff
- Add natural-language intent detection while keeping button choices
- Track recurring issues and unsuccessful routes
- Expand device-specific support
