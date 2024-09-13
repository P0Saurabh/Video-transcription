# Video Transcription Generator

This Python script automatically generates a text transcription from a video file. It extracts the audio from the video, processes it in chunks, and uses Google's Speech Recognition service to create a timestamped transcription.

## Features

- Extracts audio from video files
- Generates timestamped transcriptions
- Saves transcriptions to a text file

## Requirements

- Python 3.6 or higher
- moviepy
- SpeechRecognition

## Installation

1. Clone this repository or download the script files.

2. Install the required Python packages:

   ```
   pip install -r requirements.txt
   ```

   Note: On some systems, you might need to install additional audio processing libraries. For example:

   - On Ubuntu or Debian-based systems:
     ```
     sudo apt-get install python3-pyaudio
     ```
   - On macOS using Homebrew:
     ```
     brew install portaudio
     pip install pyaudio
     ```

## Usage

1. Place your video file in the same directory as the script, or note its full path.

2. Open the script (`video_transcription.py`) and modify the `video_path` variable with your video file's name or path:

   ```python
   video_path = "your_video.mp4"  # Replace with your video file path
   ```

3. Run the script:

   ```
   python video_transcription.py
   ```

4. The script will process the video and generate a `transcription.txt` file in the same directory.

## Output

The `transcription.txt` file will contain timestamped transcriptions in the following format:

```
start_time - end_time: transcribed text
```

For example:
```
0.00 - 3.00: Hello, welcome to the video
3.00 - 6.00: Today we'll be discussing...
```

## Limitations

- The accuracy of the transcription depends on the audio quality and the performance of the Google Speech Recognition service.
- Very long videos may take a considerable amount of time to process.
- The script requires an active internet connection to use the Google Speech Recognition service.

## Contributing

Contributions to improve the script are welcome. Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).
