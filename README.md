# 🎵 Music Transformer on JSB Chorales

This project implements and trains a **Music Transformer** on the **JSB
Chorales dataset** to learn sequence modeling for symbolic music
generation.

------------------------------------------------------------------------

## 📂 Project Structure

-   `music_transformer.ipynb` → Main Jupyter Notebook containing the
    model, training, and evaluation code.
-   `graphs/` → Contains training & evaluation plots.
    -   `accuracy.png`
    -   `perplexity.png`
    -   `trainVSval.png`
-   `final_model.pth` → Saved trained model weights.
-   `requirements.txt`
-   `README.md`
-   `LICENSE`

------------------------------------------------------------------------

## 📊 Training Results

### Accuracy

![Accuracy](graphs/accuracy.png)

### Perplexity

![Perplexity](graphs/perplexity.png)

### Training vs Validation Loss

![Training vs Validation](graphs/trainVSval.png)

------------------------------------------------------------------------

## 🏆 Final Evaluation

-   **Evaluation Loss**: \~1.835
-   **Perplexity**: \~6.26
-   **Accuracy**: \~16%

------------------------------------------------------------------------

## ⚠️ Note on Metrics

In earlier runs, the model appeared to show very high accuracy. However, this was misleading because the Music Transformer had collapsed into predicting only the **padding token**.  
Since the evaluation data contained many padding positions, the metrics were artificially inflated and did not reflect real learning.  

This issue was fixed by updating the training loop and applying **loss masking** to ignore padding tokens.  
As a result, the reported metrics are now lower but **accurately represent model performance** on musical sequence prediction.


## 🚀 How to Use

1.  Clone this repository:

    ``` bash
    git clone https://github.com/lakshinkhurana/music-transformer.git
    cd music-transformer
    ```

2.  Open the Jupyter Notebook:

    ``` bash
    pip install -r requirements.txt
    jupyter notebook music_transformer.ipynb
    ```

3.  To load the trained model:

    ``` python
    import torch
    from model import MusicTransformer  # adjust if model class is defined inside notebook

    model = MusicTransformer(...)
    model.load_state_dict(torch.load("final_model.pth", map_location="cpu"))
    model.eval()
    ```

------------------------------------------------------------------------

## 📥 Download Pretrained Model

You can download the trained Music Transformer model here:

➡️ [**final_model.pth**](final_model.pth)
