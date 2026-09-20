# BeatNet Installation Guide

Complete step-by-step guide to set up BeatNet on your system.

## Prerequisites

- **Python**: 3.8 or higher
- **pip**: Python package manager
- **git**: For cloning the repository

## Installation Steps

### Step 1: Clone the Repository

```bash
git clone https://github.com/MarGiN-7/BeatNet-AutomatedMusicGenreClassification.git
cd BeatNet-AutomatedMusicGenreClassification
```

### Step 2: Create Virtual Environment (Recommended)

**On macOS/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

**On Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

### Step 3: Install System Dependencies

**On Ubuntu/Debian:**
```bash
sudo apt-get update
sudo apt-get install -y libsndfile1 ffmpeg
```

**On CentOS/RHEL:**
```bash
sudo yum install -y libsndfile ffmpeg
```

**On Fedora:**
```bash
sudo dnf install -y libsndfile ffmpeg
```

**On macOS (with Homebrew):**
```bash
brew install libsndfile ffmpeg
```

**On Windows:**
1. Download FFmpeg from: https://ffmpeg.org/download.html
2. Download libsndfile from: https://github.com/libsndfile/libsndfile/releases
3. Add to system PATH

### Step 4: Install Python Dependencies

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### Step 5: Verify Model Files

Ensure the following files exist in the project root:
- `b.h5` (Neural network model)
- `g.pkl` (Label encoder)

If missing, download them or train your own model.

## Running the Application

```bash
streamlit run musicapp.py
```

The application will be available at: `http://localhost:8501`

## Troubleshooting

### Issue: "Command 'ffmpeg' not found"

**Solution:**
- Verify FFmpeg is installed: `ffmpeg -version`
- On Linux, ensure PATH is set correctly: `export PATH="/usr/bin:$PATH"`
- On Windows, add FFmpeg to system PATH environment variable

### Issue: "No module named 'librosa'"

**Solution:**
```bash
pip install librosa --upgrade
```

### Issue: "ModuleNotFoundError: No module named 'streamlit'"

**Solution:**
```bash
pip install streamlit --upgrade
```

### Issue: "Model file not found: b.h5"

**Solution:**
- Check if `b.h5` exists in the project root
- If missing, ensure the file was downloaded correctly
- Verify file is not corrupted (should be ~60MB)

### Issue: "libsndfile not found" (Linux)

**Solution:**
```bash
# For Ubuntu/Debian
sudo apt-get install libsndfile1

# For CentOS/RHEL
sudo yum install libsndfile

# For Fedora
sudo dnf install libsndfile
```

### Issue: "Port 8501 already in use"

**Solution:**
```bash
streamlit run musicapp.py --server.port 8502
```

## System Requirements

### Minimum
- **RAM**: 4 GB
- **Storage**: 2 GB free space
- **Processor**: Any modern CPU

### Recommended
- **RAM**: 8 GB or more
- **Storage**: 5 GB SSD free space
- **Processor**: Multi-core processor
- **GPU**: NVIDIA GPU (optional, for faster processing)

## GPU Support (Optional)

For faster predictions with NVIDIA GPU:

```bash
pip uninstall tensorflow-cpu
pip install tensorflow-gpu
```

Ensure CUDA 11.x and cuDNN are installed.

## Docker Installation (Advanced)

**Dockerfile:**
```dockerfile
FROM python:3.9-slim

WORKDIR /app

RUN apt-get update && apt-get install -y \
    libsndfile1 \
    ffmpeg \
    && rm -rf /var/lib/apt/lists/*

COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . .

EXPOSE 8501

CMD ["streamlit", "run", "musicapp.py", "--server.port", "8501", "--server.address", "0.0.0.0"]
```

**Build and Run:**
```bash
docker build -t beatnet .
docker run -p 8501:8501 beatnet
```

## Updating Dependencies

To update all packages to latest versions:

```bash
pip install --upgrade -r requirements.txt
```

## Uninstalling

To remove BeatNet and its dependencies:

```bash
# Deactivate virtual environment
deactivate

# Remove virtual environment
rm -rf venv

# Remove repository
cd ..
rm -rf BeatNet-AutomatedMusicGenreClassification
```

## Getting Help

- Check the main [README.md](README.md)
- Open an issue on GitHub
- Check Streamlit documentation: https://docs.streamlit.io/
- Check TensorFlow documentation: https://www.tensorflow.org/

## Next Steps

1. Run the application: `streamlit run musicapp.py`
2. Upload an audio file
3. Get instant genre predictions!

Enjoy using BeatNet! 🎧
