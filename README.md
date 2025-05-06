# Grammar-Scoring-Engine
Grammar Scoring Engine – Optimization Summary

This project focused on predicting grammar quality scores from spoken English audio samples. Two different models were developed and optimized during the process:

Model 1: Audio Feature-Based Regressor
Extracted acoustic features using Librosa, such as MFCCs, spectral features, and zero-crossing rate (ZCR).

Employed a stacked ensemble regressor combining SVR, Gradient Boosting, and RidgeCV.

Achieved moderate performance, but lacked direct linguistic interpretability.

Model 2: Transcription + NLP Feature-Based Regressor
Transcribed audio to text using automatic speech recognition (ASR).

Extracted linguistic features such as word count, part-of-speech (POS) tags, and average word length using NLTK.

Trained a Random Forest Regressor, which significantly improved performance.

Final Performance (Model 2)
RMSE: 0.5030

MAE: 0.4144

R² Score: 0.7695

By transitioning from low-level audio features to higher-level linguistic features derived from transcriptions, the model was able to more accurately capture grammatical correctness and align more closely with human evaluation.

