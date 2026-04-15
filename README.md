Overview

Jarvis is a Python-based voice assistant that listens for a wake word (“Jarvis”), processes natural speech, executes system commands, and responds using either predefined actions or Google Gemini AI.

It is designed for hands-free interaction with your computer using voice commands.

Features
Wake word detection (“Jarvis”)
Speech-to-text input using microphone
Text-to-speech responses
Google Gemini AI integration for general queries
Screenshot capture with timestamped filenames
Custom command system via external module
Continuous listening loop
Basic error handling for stable runtime
Requirements
Python Version
Python 3.8 or higher
Dependencies

Install required packages:

pip install speechrecognition pyttsx3 pyautogui google-generativeai pyaudio
Environment Variables

This project requires a Google Gemini API key.

Windows (PowerShell)
setx GEMINI_API_KEY "your_api_key_here"
Linux / macOS
export GEMINI_API_KEY="your_api_key_here"
Project Structure
project/
│
├── main.py              # Main voice assistant logic
├── commands.py         # Custom command registry and actions
└── README.md
How It Works
The program starts and initializes the speech engine.
It continuously listens for the wake word “Jarvis”.
When triggered, it activates command mode.
The user speaks a command.
The system processes the command in this order:
Checks predefined custom commands
If no match is found, sends input to Gemini AI
The assistant speaks the response back to the user.
Usage

Run the main script:

python main.py

Then say:

Jarvis

Followed by your command.

Commands

Custom commands are defined in commands.py.

Example behavior:

System actions (open apps, control system tasks)
Screenshot capture
Any user-defined automation

If no command matches, the assistant uses AI to respond.

Exit

To stop the assistant, say:

exit

Error Handling

The system handles:

Microphone timeouts
Speech recognition errors
API failures from Gemini
Unexpected runtime exceptions
Requirements Notes
Requires a working microphone
Internet connection required for:
Speech recognition
Gemini AI responses
Future Improvements
Add GUI interface
Improve wake word detection accuracy
Expand command library
Add offline mode support
Add multi-language support
License

This project is open-source and can be modified for personal or educational use.