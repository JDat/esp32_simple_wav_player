# esp32_simple_wav_player
no I2S device required. Just connect ESP32 and speaker with two lines (GND / GPIO25).

## Description

It is a simple Wev Player that lets ESP32 speak fixed phrases, and is prepared as a base for making clocks and weather forecasts.
Even if there is no external circuit, you can get sound just by connecting the speaker. Allowed you to hear and compare audio from multiple sampling rates for testing.

## Features

--Support for multiple sampling rates (4KHz, 8KHz, 16KHz, ...)
--8bit / 16bit data size support
--Continuous playback of multiple data
――...

## Requirement

--ESP32 x 1
--Speaker x 1
-(2KΩ semi-fixed resistor, 0.1μ capacitor)


## Usage

1. Prepare a Wav file in PCM format with software such as Audacity. Since the information is obtained from the file header, it is not set to RAW (header-less).
2. Convert the audio file to text with software such as HxD. Output the data in C language array format and make it include data.
2.1 In linux you use xxd tool for converting: xxd - i inputfile.wav audiodata.h Then make minor sample array edit.

## Installation

Compile with Arduino IDE and Arduino core for the ESP32 and transfer to ESP32.

## Author

kghrlabo (http://kghr.blog.fc2.com/)

## License

TBD 
