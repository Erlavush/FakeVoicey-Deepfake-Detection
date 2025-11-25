# FakeVoicey: Deepfake Audio Detection Benchmark

### 🎓 University of Southeastern Philippines - Machine Learning Learning Evidence

**Authors:** Earl Josh B. Delgado, John Marcellin E. Tan, Leah O. Pelias, Maureen M. Villamor

## 📄 Abstract
Voice generation technology has evolved exponentially by 2025. This study benchmarks four deep learning architectures (**ResNet-18, Bi-LSTM, Wav2Vec 2.0, AST**) against the "Modern-Wild 2025" dataset, containing deepfakes from ElevenLabs and Edge-TTS. Our results indicate that the **Audio Spectrogram Transformer (AST)** is the most robust defense, achieving **82.33% accuracy** and an **EER of 11.74%**, while traditional Bi-LSTMs failed to generalize.

## 📊 Key Results
| Model | Accuracy | AUC | EER |
| :--- | :--- | :--- | :--- |
| **AST** | **82.33%** | 0.937 | **11.74%** |
| ResNet-18 | 79.07% | **0.969** | 10.00% |
| Wav2Vec 2.0 | 70.00% | 0.792 | 25.65% |
| Bi-LSTM | 56.28% | 0.627 | 40.00% |

## 🧠 Architectures Implemented
1.  **Bi-LSTM:** Sequential processing using MFCCs.
2.  **ResNet-18:** Computer Vision approach using Log-Mel Spectrograms.
3.  **Wav2Vec 2.0:** End-to-End Transformer on raw waveforms.
4.  **AST (Audio Spectrogram Transformer):** Attention-based processing on spectrogram patches.

## ⚙️ Methodology
*   **Sampling Rate:** Standardized to 16kHz (Librosa).
*   **Augmentation:** Gaussian Noise, Gain, Pitch Shift (Audiomentations).
*   **Explainability:** Attention Map Visualizations implemented for AST.

## 🚀 How to Run
1. Open the `.ipynb` file in Google Colab.
2. Upload the dataset zip file to your Google Drive.
3. Change the `ZIP_PATH` variable to point to your data.
4. Run all cells.

## 📂 Dataset
*   **Training:** ASVspoof 2019 Logical Access (Subset).
*   **Testing:** Custom "Modern-Wild" dataset (LibriSpeech + ElevenLabs + EdgeTTS).
