**Speech Recognition with SaraKIT**

SaraKIT is equipped with three microphones and a specialized audio processor that clarifies the voice and supports speech recognition on Raspberry Pi, offering a significant leap in enabling offline, cloud-independent voice command functionalities. While many tools for speech recognition are available online, with cloud-based data analysis tools like Google Speech to Text being among the best and most efficient as discussed in another guide of mine, this article focuses on offline speech recognition—without the need for an internet connection.

In my search for the best and simplest-to-configure tool, I believe I've found a noteworthy solution currently recommended for offline speech recognition - Vosk API:

**Vosk Speech Recognition Toolkit**
Vosk is an offline open-source speech recognition toolkit, facilitating speech recognition in over 20 languages and dialects including English, German, French, Spanish, and many more. Its models are compact (around 50 Mb) but support continuous large vocabulary transcription, offer zero-latency response with a streaming API, feature reconfigurable vocabulary, and identify speakers. Vosk caters to a range of applications from chatbots and smart home devices to virtual assistants and subtitle creation, scaling from small devices like Raspberry Pi or Android smartphones to large clusters.

**Vosk Homepage:** [https://alphacephei.com/vosk/](https://alphacephei.com/vosk/)
**GitHub Vosk:** [https://github.com/alphacep/vosk-api](https://github.com/alphacep/vosk-api)

**Installing on SaraKIT:**
Assuming the basic SaraKIT drivers are already installed ([https://sarakit.saraai.com/getting-started/software](https://sarakit.saraai.com/getting-started/software)), follow these steps to install:

```bash
sudo apt-get install pip
sudo apt-get install -y python3-pyaudio
sudo pip3 install vosk

git clone https://github.com/SaraEye/SaraKIT-Speech-Recognition-Vosk-Raspberry-Pi SpeechRecognition
cd SpeechRecognition
```

To use a language other than English, download the required language model from [https://alphacephei.com/vosk/models](https://alphacephei.com/vosk/models) and place it in the `models` directory.

Start speech recognition by running:

```bash
python SpeechRecognition.py
```

The effects of this simple yet powerful script can be seen in the video below:

https://github.com/SaraEye/SaraKIT-Speech-Recognition-Vosk-Raspberry-Pi/assets/35704910/5c7b53b0-90b7-4e00-9055-686648546965

Project page: https://sarakit.saraai.com/example-of-use/speech-recognition
