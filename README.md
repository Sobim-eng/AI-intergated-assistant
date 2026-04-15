# Jarvis Voice Assistant

## Overview
Jarvis is a Python-based voice assistant built to listen for a wake word, process voice commands, execute system actions, and respond using either predefined commands or Google Gemini AI.

## Features
- Voice recognition using microphone
- Wake word activation ("Jarvis")
- Text-to-speech responses
- Google Gemini AI integration
- Screenshot capture with timestamped filenames
- Custom command system via external module (`commands.py`)
- Continuous listening loop
- Random spoken responses for natural interaction
- Graceful exit using voice command ("exit")
- Basic error handling for stability

## Requirements
- Python 3.8 or higher
- Working microphone
- Internet connection

## Installation
Install required dependencies:
pip install speechrecognition pyttsx3 pyautogui google-generativeai pyaudio

## Environment Setup
This project requires a Google Gemini API key.

Windows (PowerShell):
setx GEMINI_API_KEY "your_api_key_here"

Linux / macOS:
export GEMINI_API_KEY "your_api_key_here"

## Project Structure
project/
│
├── main.py # Main voice assistant logic
├── commands.py # Custom command registry and actions
└── README.md

## How It Works
The program starts and initializes speech recognition and TTS engine.
It continuously listens for the wake word "Jarvis".
When detected, it activates command mode.
The user speaks a command.
The system processes input:
If it matches a predefined command, it executes it.
Otherwise, it sends the input to Google Gemini AI.
The response is spoken back to the user.

## Usage
Run the program:
python main.py

Then say:
Jarvis

Followed by your command.

## Exit
Say:
exit

## Notes
Requires a working microphone
Internet connection is required for speech recognition and AI responses
The assistant runs continuously until explicitly stopped

## Error Handling
The system handles:
Speech recognition failures
Microphone timeouts
API errors from Gemini
Unexpected runtime exceptions