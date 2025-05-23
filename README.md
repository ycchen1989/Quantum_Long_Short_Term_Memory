# QLSTM for Time-Series Forecasting with Quantum Circuits

This repository implements a **Quantum Long Short-Term Memory (QLSTM)** model for time-series forecasting. It integrates parameterized quantum circuits (VQCs) into a classical LSTM architecture using [PennyLane](https://pennylane.ai/) and [PyTorch](https://pytorch.org/).

---

## 🚀 Highlights

- 🧠 **Custom QLSTMCell** with VQC-based gates (`input`, `forget`, `cell`, `output`)
- 🔁 Sequence modeling using `CustomLSTM`
- 📉 Real-time loss tracking and automatic PDF plotting
- 🧪 Tested on damped simple harmonic motion (SHM) synthetic dataset
- 💾 Supports model/result saving for reproducibility

---

## 🧪 Dataset

We use a toy **damped simple harmonic motion** dataset defined in `data/damped_shm.py`, which generates:

- Input: `[batch_size, seq_len, 1]` time-series
- Target: `[batch_size, 1]` next-step prediction

---

## 🚀 How to Run

```bash
python QLSTM_v0.py
```

Running the script will:

- 🧠 Train a **QLSTM model** for **100 epochs**
- 💾 Save plots and model checkpoints under the folder:  
  `QLSTM_TS_MODEL_DAMPED_SHM_1/`
- 📊 Generate the following visualizations:
  - Training/testing **loss curves**
  - **Ground truth** vs. **predicted output** plots

---


## 📚 Citation / Reference

If you find this repository useful for your research or teaching, please consider citing the following paper:

```bibtex
@inproceedings{chen2022quantum,
  title={Quantum long short-term memory},
  author={Chen, Samuel Yen-Chi and Yoo, Shinjae and Fang, Yao-Lung L},
  booktitle={Icassp 2022-2022 IEEE international conference on acoustics, speech and signal processing (ICASSP)},
  pages={8622--8626},
  year={2022},
  organization={IEEE}
}
