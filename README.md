# 🎧 VGG16 for Audio Classification

This repository demonstrates how to use a **VGG16 convolutional neural network** to classify audio signals by first converting them into **Mel spectrograms** (image-like representations of sound). It is a simple yet powerful approach that bridges audio and computer vision using deep learning.

---

## 📌 Features

- 🔊 Converts audio files to spectrograms (Mel, MFCC, etc.)
- 🧠 Uses transfer learning with pretrained VGG16
- 🧪 Trains and evaluates on custom audio datasets
- 📈 Plots training loss and accuracy
- 📁 Simple dataset structure: one folder per class

---

## 🧰 Installation

Clone the repo:

```bash
git clone https://github.com/haroon423/VGG16-for-audio-classification.git
cd VGG16-for-audio-classification

pip install -r requirements.txt

📂 Dataset Structure
Organize your dataset as follows (2-class classification):

dataset/
├── human/
│   ├── sample1.wav
│   ├── sample2.wav
│   └── ...
├── machine/
│   ├── voicemail1.wav
│   ├── voicemail2.wav
│   └── ...

human/ → contains real human speech recordings

machine/ → contains synthetic or pre-recorded machine voicemail audio

This structure allows the model to learn to distinguish between natural human voice and automated voicemail systems.

🚀 How to Run
1. Convert Audio to Spectrograms
Run the spectrogram generator:
python convert_audio_to_spectrogram.py
This will generate .png files of spectrograms in an output folder, grouped by class.

2. Train VGG16 Model
python train.py
You can customize:

Learning rate

Epochs

Batch size

Data path

🧠 Model
📚 Base Model: VGG16 from torchvision.models

🔁 Transfer Learning: Fine-tunes final layers on spectrogram dataset

🏷️ Output: Classifies audio into predefined categories

📊 Results
Accuracy: >90% on clean, labeled datasets

Works best with clear audio samples and well-separated classes

📝 Requirements
See requirements.txt or below.

📄 License
This project is licensed under the MIT License.

👨‍💻 Author
Haroon Khan
AI Engineer | Audio, Vision, NLP
📧 hk4897286@gmail.com
🔗 GitHub
