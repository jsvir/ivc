Audio samples for the paper: Provable Speech Attributes Conversion via Latent Independence

[![Arxiv Paper](https://img.shields.io/badge/arXiv-2510.05191-red)](https://arxiv.org/abs/2510.05191)

Model performance comparison after expanding the training data to include a larger and more diverse speaker pool. The same architecture was retrained on multiple datasets:
  - VCTK (110 speakers)
  - LibriTTS train-clean-360 (904)
  - LibriSpeech train-clean-100 (251)
  - ESD English (10)
    
totaling 1,265 speakers. During inference, the reference speaker is provided using a single full-length utterance, whereas training is performed on 3-second audio chunks for 300 epochs.

| Model     | WER↓  | CER↓  | EER↑  |
|-----------|-------|-------|-------|
| Target*   | 5.96  | 2.38  | 50.00 |
| YourTTS*  | 11.93 | 5.51  | 25.32 |
| Free-VC*  | 7.61  | 3.17  | 8.97  |
| KNN-VC    | 17.37 | 8.55  | 24.01 |
| IVC (LibriSpeech-train-clean-100)| 11.38 | 4.92  | 10.77 |
| IVC (More data)    | 9.11  | 3.78  | 16.50 |

