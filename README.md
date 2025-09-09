# 🎶 GTZAN Music Genre Classification

This project classifies songs into **10 music genres** by exploring two approaches:

1. **Tabular Features (MFCCs, Chroma, Spectral Contrast, Tonnetz)** → Random Forest Classifier  
2. **Spectrogram Images** → Transfer Learning with **ResNet18 (CNN)**

Finally, we integrate the models into a **Gradio Interface** to test audio clips interactively.

---

## 📂 Dataset Structure
The dataset provides:
- **Audio files** (`genres_original/`) – WAV format, 30s each.  
- **Spectrogram images** (`images_original/`) – visual representation of the audio.  
- **Pre-computed features** (`features_30_sec.csv` and `features_3_sec.csv`).  

**Genres included**:  
`blues, classical, country, disco, hiphop, jazz, metal, pop, reggae, rock`

---

## 🛠️ Tools & Libraries
- **Python**
- **Librosa** – audio feature extraction  
- **Scikit-learn** – Random Forest, pipeline, evaluation  
- **PyTorch** – CNN, ResNet18 transfer learning  
- **Matplotlib / Seaborn** – visualization  
- **Gradio** – interactive demo  

---

## ⚙️ Workflow
1. **Data Exploration** – inspect CSV features and genres.  
2. **Preprocessing**  
   - Extract MFCCs, Chroma, Spectral Contrast, Tonnetz features.  
   - Generate spectrograms for CNN input.  
3. **Model Training**  
   - Train **Random Forest** on tabular features.  
   - Fine-tune **ResNet18** (transfer learning) on spectrogram images.  
4. **Evaluation** – accuracy, confusion matrix, per-class performance.  
5. **Deployment** – Gradio app to test audio files.  

---

## 📊 Results (Example)
| Model          | Accuracy (Val) |
|----------------|----------------|
| Random Forest (tabular) | ~0.70 |
| ResNet18 Transfer (spectrograms) | ~0.80–0.85 |

*(Numbers depend on training setup and epochs.)*

---

## 🚀 Gradio Interface
Users can upload an **MP3/WAV** file and choose:
- **Tabular Model** (faster, less accurate)  
- **Transfer Model** (CNN, higher accuracy)  

**Example:**  

<img width="1899" height="702" alt="image" src="https://github.com/user-attachments/assets/90ef0140-c1ef-4b25-a46c-dde8b47cdcaf" />



---

## 🖼️ Spectrogram Example
Here’s a generated **mel-spectrogram** for a classical music sample:
![5911252576152701765](https://github.com/user-attachments/assets/d514e557-e0d0-460e-88ba-1ebe333742e1)

