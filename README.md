# Image-to-Image Translation using GANs

### CycleGAN & Pix2Pix (Sketch ↔ Photo | Sketch → Image)

This repository contains two deep learning projects implemented using **PyTorch**:

1. **CycleGAN** – Unpaired Image-to-Image Translation (Sketch ↔ Photo)
2. **Pix2Pix** – Paired Image-to-Image Translation (Face & Anime Sketch → Image)

Both projects were developed collaboratively and demonstrate the power of **Generative Adversarial Networks (GANs)** for visual transformation tasks.

---

## 🚀 Project Overview

### 1. CycleGAN (Unpaired Translation)

* Converts:

  * Sketch → Photo
  * Photo → Sketch
* Works **without paired data**
* Uses:

  * Cycle Consistency Loss
  * Identity Loss
  * PatchGAN Discriminators

### 2. Pix2Pix (Paired Translation)

* Converts:

  * Face Sketch → Real Face
  * Anime Sketch → Colored Image
* Uses **paired datasets**
* Architecture:

  * U-Net Generator (with skip connections)
  * PatchGAN Discriminator
* Loss Functions:

  * Adversarial Loss
  * L1 Reconstruction Loss

---

## 🛠️ Features

* Custom dataset loaders for both paired and unpaired data
* Data preprocessing and augmentation
* Mixed Precision Training (AMP) for performance optimization
* Multi-GPU support (DataParallel)
* Model checkpointing
* Training loss visualization
* Evaluation metrics:

  * SSIM (Structural Similarity Index)
  * PSNR (Peak Signal-to-Noise Ratio)
* Interactive **Gradio Web App** for real-time inference

---

## 📂 Project Structure

```
├── cyclegan.py              # CycleGAN implementation
├── pix2pix.py              # Pix2Pix implementation
├── checkpoints/            # Saved model weights
├── images/                 # Generated samples
├── results/                # Output visualizations
├── README.md               # Project documentation
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/your-username/gan-image-translation.git
cd gan-image-translation
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 📊 Datasets

### CycleGAN

* TU-Berlin Sketch Dataset
* Sketchy Dataset
* QuickDraw Dataset
* Synthetic data (auto-generated if needed)

### Pix2Pix

* CUHK Face Sketch Dataset (CUFS)
* Anime Sketch Colorization Dataset

> Note: Update dataset paths in the code based on your environment.

---

## ▶️ Training

### CycleGAN

```bash
python cyclegan.py
```

### Pix2Pix

```bash
python pix2pix.py
```

---

## 📈 Results

* Realistic image generation from sketches
* Strong structural consistency in CycleGAN
* High-quality reconstruction in Pix2Pix
* Visual outputs saved during training
* Loss curves generated for analysis

---

## 🧪 Evaluation Metrics

| Metric | Description                                            |
| ------ | ------------------------------------------------------ |
| SSIM   | Measures structural similarity (closer to 1 is better) |
| PSNR   | Measures image quality (higher is better)              |

---

## 🌐 Inference (Gradio App)

Run the app to test the model interactively:

```bash
python app.py
```

* Upload an image
* Select translation direction
* Get real-time generated output

---

## 💡 Key Learnings

* Difference between **paired vs unpaired image translation**
* Importance of **cycle consistency** in unpaired learning
* Role of **skip connections** in preserving details
* Training stability techniques in GANs

---

## 🤝 Collaboration

This project was developed collaboratively as part of deep learning practice and experimentation with GAN architectures.

---

## 📌 Future Improvements

* Add FID score for better evaluation
* Improve dataset diversity
* Deploy as a web application
* Optimize training time

---

## 📜 License

This project is open-source and available under the MIT License.

---

## ⭐ Support

If you found this project useful, consider giving it a star on GitHub!

---
