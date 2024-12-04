PyPiperTTS-win: A Python Interface for Piper Text-to-Speech (windows)
===========================================================
PyPiperTTS-win is a Python library that provides a simple and intuitive interface to the Piper text-to-speech system. It allows you to generate high-quality speech from text using pre-trained models. Optimized for Windows OS.

Installation
-----
To use PyPiperTTS, you'll need to have Python 3.6 to Python 3.10 installed on your system.
Download the Piper package for Windows here:
https://github.com/rhasspy/piper/releases/download/2023.11.14-2/piper_windows_amd64.zip
Unzip and move the Folder (Piper) to your application environment folder (.venv)

You can install the additional required dependencies using pip:
```Bash
pip install -r requirements.txt
```
Usage
-----
### Initializing the PyPiper Object
To start using PyPiperTTS, create an instance of the PyPiper class:
```Python
from pypipertts import PyPiper

piper = PyPiper()
```
### Generating Speech
You can generate speech from text using the tts method:
```Python
output_file = piper.tts("Hello, world!")
print(output_file)
```
This will generate a WAV file containing the synthesized speech.

### Streaming Speech
You can also stream the synthesized speech in real-time using the stream_tts method:
```Python
streamed_audio = piper.stream_tts("Hello, world!")
# play streamed audio
```
### Saving and Loading Model Settings
You can save and load model settings using the save_set and load_set methods:
```Python
# Save model settings
set_file = piper.save_set("en_US-joe-medium", 1, 1, 1, 1)

# Load model settings
model, length, noise, width, pause = piper.load_set(set_file)
print(model, length, noise, width, pause)
```
Requirements
------------
- Python 3.6 or later
- Piper text-to-speech for Windows (https://github.com/rhasspy/piper/releases/download/2023.11.14-2/piper_windows_amd64.zip)
- pydub library for audio processing
- requests library for downloading models

License
-------
PyPiperTTS-win is released under the MIT License.
