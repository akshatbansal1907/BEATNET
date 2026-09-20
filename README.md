# 🎧 BeatNet - Automated Music Genre Classification

> AI-powered music genre recognition powered by deep learning

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-Latest-red?logo=streamlit)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.0+-orange?logo=tensorflow)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

## 🎵 What is BeatNet?

BeatNet is an intelligent web application that **instantly identifies music genres** using artificial intelligence. Upload any audio file (MP3 or WAV), and let the AI analyze the audio patterns to predict the genre with confidence scoring!

Perfect for:
- 🎤 Music categorization automation
- 📊 Audio analytics projects
- 🎓 Learning deep learning & audio processing
- 🚀 Building music recommendation systems

## ✨ Quick Features

| Feature | Description |
|---------|-------------|
| 🤖 **AI-Powered** | Deep learning neural network for accurate predictions |
| ⚡ **Real-time** | Get genre predictions in seconds |
| 📱 **Web Interface** | Beautiful, interactive Streamlit UI |
| 🔊 **Multi-format** | Supports MP3 and WAV files up to 25MB |
| 📊 **Confidence Scores** | Know how confident the AI is in its predictions |
| 🎨 **Modern UI** | Sleek, user-friendly interface |

## 🚀 Getting Started in 3 Steps

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/MarGiN-7/BeatNet-AutomatedMusicGenreClassification.git
cd BeatNet-AutomatedMusicGenreClassification
```

### 2️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 3️⃣ Run the App
```bash
streamlit run musicapp.py
```

Visit `http://localhost:8501` and start predicting! 🎉

## 📋 Requirements

**Python Packages:**
- streamlit
- tensorflow-cpu
- librosa
- scikit-learn

**System Dependencies:**
- ffmpeg
- libsndfile1

See [INSTALLATION_GUIDE.md](INSTALLATION_GUIDE.md) for detailed setup for all OS.

## 🎯 How It Works

```
Upload Audio → Mel-Spectrogram Extraction → Neural Network → Genre Prediction 🎵
```

1. **Audio Processing** - Converts audio to visual representation (Mel-Spectrogram)
2. **Feature Extraction** - Analyzes 128 frequency bands across time
3. **Neural Network** - Pre-trained CNN processes the features
4. **Classification** - Returns predicted genre + confidence score

## 💻 Tech Stack

- **Frontend**: [Streamlit](https://streamlit.io/) - Fast web app framework
- **AI/ML**: [TensorFlow & Keras](https://www.tensorflow.org/) - Deep learning
- **Audio**: [Librosa](https://librosa.org/) - Audio feature extraction
- **ML Utils**: [Scikit-learn](https://scikit-learn.org/) - Label encoding

## 🎪 Fun Ideas to Extend BeatNet

- 🎶 Create a **Music Playlist Generator** based on genre
- 📈 Build a **Mood Tracker** - what genre for what mood?
- 🎮 Make a **Guess-the-Genre Game** - train your ear!
- 📊 Create **Statistics Dashboard** - most detected genres
- 🔗 Integrate with **Spotify API** for real-time playlists
- 🌍 Deploy on **Streamlit Cloud** for free hosting

## 📂 Project Structure

```
BeatNet-AutomatedMusicGenreClassification/
├── musicapp.py              # Main application
├── requirements.txt         # Python dependencies
├── packages.txt             # System dependencies
├── b.h5                     # Pre-trained model (download needed)
├── g.pkl                    # Label encoder (download needed)
├── README.md                # This file
├── INSTALLATION_GUIDE.md    # Setup instructions
└── LICENSE                  # MIT License
```

## ⚙️ Model Files Required

To run the app, download these from the original repo:
- **b.h5** (61.4 MB) - Pre-trained neural network
- **g.pkl** (599 bytes) - Genre label encoder

Place them in the project root directory.

## 🎓 Supported Genres

The model can classify music into multiple genres including:
```
Pop • Rock • Hip-Hop • Jazz • Classical • Electronic • Blues • Country
(and more depending on training data)
```

## 📸 Screenshots

| Upload | Analyzing | Results |
|--------|-----------|---------|
| Upload your track | 🔄 Processing... | 🎉 Genre Detected! |

## 🐛 Troubleshooting

**"File not found" error?**
- Ensure `b.h5` and `g.pkl` are in the project root

**"FFmpeg not found"?**
- Install: `sudo apt install ffmpeg` (Linux) or `brew install ffmpeg` (macOS)

**"File too large"?**
- Max file size is 25MB

See [INSTALLATION_GUIDE.md](INSTALLATION_GUIDE.md) for more solutions.

## 🚀 Deployment

### Deploy for Free on Streamlit Cloud

1. Push code to GitHub (done! ✅)
2. Go to [Streamlit Cloud](https://streamlit.io/cloud)
3. Connect your GitHub repo
4. Select `musicapp.py` as entry point
5. Deploy! 🎉

## 🤝 Contributing

Found a bug? Have an idea? Contributions welcome!

1. Fork the repo
2. Create a feature branch: `git checkout -b feature/cool-feature`
3. Commit: `git commit -am 'Add cool feature'`
4. Push: `git push origin feature/cool-feature`
5. Open a Pull Request

## 📄 License

MIT License - Feel free to use this project for personal or commercial purposes.


## 📞 Support

- 🐛 Found an issue? Open a GitHub Issue
- 💡 Have suggestions? Let us know!
- ⭐ Like it? Give it a star!

## 🎉 Try It Now!

```bash
git clone https://github.com/MarGiN-7/BeatNet-AutomatedMusicGenreClassification.git
cd BeatNet-AutomatedMusicGenreClassification
pip install -r requirements.txt
streamlit run musicapp.py
```

Upload your favorite song and watch the AI identify its genre! 🎵✨

---
