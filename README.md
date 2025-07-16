# 🎵 Music Transformer: Generating Music with Long-Term Structure

This repository is a reimplementation of the research paper:  
📄 [Music Transformer: Generating Music with Long-Term Structure](https://arxiv.org/abs/1809.04281) by Huang et al., 2018.

> This model leverages the Transformer architecture with a novel **relative positional encoding** mechanism to generate coherent and structured musical sequences over long time spans.

---

## 🚀 Features

- Transformer-based architecture optimized for music generation.
- Support for **relative positional self-attention** for capturing long-term dependencies.
- Trained on MIDI-based datasets (e.g., MAESTRO, JSB Chorales).
- Support for both training and inference.
- Generates symbolic music in MIDI format.

---

## 🧠 Paper Contributions Summary

- Proposed a **relative attention mechanism** to overcome limitations of absolute position encodings for musical data.
- Demonstrated the model's capability to generate longer and more musically coherent sequences than baseline models.
- Introduced **event-based representation** of MIDI music for efficient tokenization.

---

## 🗂️ Project Structure

```bashmusic-transformer/
│
├── data/
│   ├── jsb_chorales/
│   └── piano_midi/
│
├── preprocessing/
│   ├── midi_parser.py
│   ├── chorale_converter.py
│
├── model/
│   ├── transformer.py
│   ├── relative_attention.py
│
├── training/
│   ├── train_baseline.py
│   ├── train_relative.py
│
├── evaluation/
│   ├── eval_nll.py
│   ├── generate_music.py
│   └── visualize_attention.py
│
├── outputs/
│   ├── generated/
│   ├── logs/
│
├── README.md
└── requirements.txt

````

## 📦 Installation

```bash
git clone https://github.com/yourusername/music-transformer.git
cd music-transformer
pip install -r requirements.txt
```

**Main dependencies:**

* `torch`
* `pretty_midi`
* `numpy`
* `tqdm`
* `pytorch-lightning` *(optional)*

---
## Week 1

- 📖 **Read the Paper Thoroughly**  
  Gain a complete understanding of the Music Transformer paper. Focus on:
  - The motivation behind using relative attention
  - Data representation methods for JSB Chorales and Piano-e-Competition
  - Transformer architecture modifications
  - Evaluation methods and sample generation

- 📦 **Dataset Collection**  
  - Download the [JSB Chorales dataset](https://github.com/czhuang/JSB-Chorales-dataset)
  - Download the MIDI files for the [Piano-e-Competition dataset](http://www.piano-e-competition.com/)

- 🧹 **Prepare for Data Preprocessing**  
  - Study the event-based encoding scheme used in the paper
  - Understand how sustain pedal, timing, and velocity are handled in MIDI preprocessing
  - Plan the pipeline for converting raw MIDI to token sequences



## 🧠 Credits

* Original authors: [Anna Huang et al.](https://magenta.tensorflow.org/music-transformer)
* Reimplementation by: [Your Name](https://github.com/yourusername)
* Inspired by: Magenta's official implementation and community forks

---

## 📨 Contact

For queries, issues, or suggestions:
📧 [lakshinkhurana@gmail.com](mailto:lakshinkhurana@gmail.com)
👜 LinkedIn: [@yourhandle](https://twitter.com/yourhandle)

---

## 🪄 License

MIT License. See `LICENSE` for details.

```

---

Let me know if you’d like:
- A Colab notebook
- Web UI with Streamlit/Gradio
- Tokenizer and generation samples
- Hugging Face integration

I can help with all of those.
```
