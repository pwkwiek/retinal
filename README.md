# Retinal Vessel Segmentation Using Color Space Optimization and Attention U-Net
*Color Me Vascular: Deep Learning with a Touch of Contrast*

##

Accurate segmentation of retinal blood vessels is vital for early detection of diseases such as diabetic retinopathy and hypertension. This project presents a deep learning-based approach using an optimized **Attention U-Net** architecture trained on contrast-enhanced image patches (256×256), with a focus on evaluating the impact of **color space representation** on segmentation performance.

### 🧠 Key Features

* 🔍 **Color Space Exploration**: Systematic comparison of 7 image channels, each selected as the most informative from **6 color spaces** (RGB, YUV, HSV, HLS, CIELab, YCrCb) and a grayscale baseline.
* 🎯 **CLAHE Preprocessing**: Enhanced vessel visibility and reduced noise using **Contrast Limited Adaptive Histogram Equalization**.
* 📊 **Top Results**:

  * **Y channel (YUV)** achieved best performance with an average **Dice coefficient of 0.879** on test patches, significantly outperforming grayscale (0.835).
  * On full-size images, Dice scores reached **0.912** with **pixel accuracy > 0.979**.
* ⚖️ **Custom Loss Function**: Combines **Binary Cross-Entropy (BCE)** with **Dice Loss** for balanced learning and shape-aware predictions.
* 🧩 **Robust Architecture**: Leverages attention gates to focus on vessel structures, improving performance across varying image representations.

### 📁 Contents

* channels.ipynb: generate datasets based on channels of various color space models
* net.ipynb: Attention U-Net Architecture; training + testing; addapt to whole image prediction

### 💡 Highlights

This work demonstrates that **color channel selection plays a critical role** in deep learning segmentation tasks. With optimal preprocessing and architecture design, the proposed method offers a strong foundation for **automated retinal image analysis** in clinical decision support systems.
