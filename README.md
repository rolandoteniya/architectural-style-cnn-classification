# Architectural Style Classification using Deep Convolutional Neural Networks
> **Applied AI Project | University of Liverpool**

## 🖼️ Project Overview
This project addresses the complex task of classifying architectural elements (e.g., domes, stained glass, flying buttresses) into 10 distinct categories. I implemented a custom-designed, parameter-efficient CNN and benchmarked it against three transfer learning strategies using **ResNet18**.

### **The Result:**
The **Fine-tuned ResNet18** model achieved a **92.58% test accuracy**, demonstrating robust generalisation. Meanwhile, my **Custom CNN** proved to be the most efficient, achieving competitive results with a fraction of the parameters.

---

### **📄 [View Full Research Report (PDF)](./Architectural_Style_CNN_Analysis.pdf)**

---

## 🛠️ Tech Stack
* **Deep Learning Framework:** `PyTorch` (torchvision)
* **Image Processing:** `PIL`, `OpenCV`
* **Data Handling:** `Pandas`, `NumPy`
* **Visualisation:** `Seaborn`, `Matplotlib`

## 🧪 Methodology & Architecture Innovation
* **Custom CNN Design:** Utilised **Depthwise Separable Convolutions** to decouple spatial filtering from channel mixing, significantly reducing computational cost without sacrificing representational depth.
* **Benchmarking Strategy:** Compared four distinct approaches:
  1. Fine-tuned ResNet18 (Best Performance)
  2. ResNet18 trained from scratch
  3. Custom CNN (Highest Efficiency)
  4. ResNet18 as a Feature Extractor
* **Data Augmentation:** Implemented dynamic transformations (Random Horizontal Flip, Rotation, and Colour Jitter) to prevent overfitting and simulate variations in architectural photography.
* **Class Imbalance Handling:** Deployed **Weighted Cross-Entropy Loss** to ensure the model accurately identified rarer architectural features like 'Flying Buttresses'.

## 📈 Key Results
| Model Strategy | Val Accuracy | Analysis |
| :--- | :--- | :--- |
| **ResNet18 (Fine-tuning)** | **93.80%** | Best performer; leveraged transfer learning for high-level semantic features. |
| **ResNet18 (Scratch)** | 86.74% | Strong performance after extended training epochs. |
| **Custom CNN** | 78.92% | **Most Efficient**; high accuracy per parameter count. |
| **ResNet18 (Feature Extr.)** | 75.45% | Proved that frozen ImageNet features require fine-tuning for this domain. |

## ⚙️ Professional Reflection & Growth
* **Interpretability:** Used **Confusion Matrix analysis** to identify visual ambiguities between 'Apse' and 'Flying Buttress' categories, providing insights into shared geometric structures.
* **Optimisation:** Implemented **Early Stopping** and **ReduceLROnPlateau** schedulers to settle the model into finer minima during training.
