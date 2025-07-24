# 🎧 MP3 Transcription Using Whisper (Faster-Whisper) on Kaggle

This project shows you how to transcribe MP3 audio files into text using OpenAI's Whisper model via the efficient [faster-whisper](https://github.com/guillaumekln/faster-whisper) library, all running on **Kaggle’s free GPU notebooks**.

---

## 🛠 Features
- Convert MP3 audio to mono 16kHz WAV
- Automatically split audio into chunks based on silence
- Transcribe each chunk using the `large` version of Whisper
- Save final transcript to `.txt` file

---

## 🚀 Getting Started on Kaggle

### 1️⃣ Create a Kaggle Account
- Go to [https://www.kaggle.com](https://www.kaggle.com)
- Click **Sign Up** and follow the instructions
- Verify your email to activate your account

---

### 2️⃣ Create a Kaggle Notebook

1. Visit: [https://www.kaggle.com/code](https://www.kaggle.com/code)
2. Click **"New Notebook"**
3. Set:
   - **Environment:** "Notebook"
   - **Accelerator:** GPU (under “Settings” → "Accelerator")
4. Click **"Save"**

---

### 3️⃣ Upload Your MP3 File

1. In the left sidebar of the notebook editor, click the **folder icon**
2. Click the **Upload** button
3. Select your `.mp3` file and upload it
4. Once uploaded, note the path (e.g. `/kaggle/input/audio.mp3`)

---

### 4️⃣ Install Dependencies

In the first cell of your notebook, run:

```python
!pip install faster-whisper pydub librosa soundfile
```

---

### 5️⃣ Paste the Python Script

- Copy and paste the full transcription script from this repository into a new notebook cell
- Update the MP3 path to match your uploaded file (e.g. `/kaggle/input/audio.mp3`)

---

### 6️⃣ Run the Notebook

- Click **"Run All"** or run cells step by step
- The final output will be saved as `whisper_large_transcript.txt` in `/kaggle/working`
- You can download it from the file explorer panel

---

## 📁 Output

A plain text file containing the full transcription of your MP3 audio:
```
/kaggle/working/whisper_large_transcript.txt
```

---

## ⚙️ Customization

- Change `top_db=30` to adjust silence detection sensitivity
- Use `"medium"` or `"small"` models in place of `"large"` for faster performance
- Change language by modifying `language="en"` in the `model.transcribe()` call

---

## 🤖 Dependencies

- `faster-whisper`
- `pydub`
- `librosa`
- `soundfile`

---

## 📌 Notes

- Kaggle provides **free NVIDIA T4 or P100 GPUs**, which are compatible with Whisper.
- If you face an issue with file paths, make sure you're referencing the correct file in `/kaggle/input/` or `/kaggle/working/`.

---

## 🧠 Credits

Built with 💡 by [Ahmedkdk24]

Inspired by OpenAI's Whisper and optimized using [faster-whisper](https://github.com/guillaumekln/faster-whisper)
