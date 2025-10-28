# Leukemia-
Leukemia cancer segmentation 
🧬 Leukemia Cell Segmentation using Deep Learning

This project applies advanced deep learning architectures to automatically segment leukemia cells from microscopic blood images, aiming to support early medical diagnosis and clinical image analysis.

🔍 Overview

I trained and evaluated multiple semantic segmentation models — U-Net, Feature Pyramid Network (FPN), Pyramid Scene Parsing Network (PSPNet), and DeepLabV3 — all built on a ResNet50 encoder.
Each model was tested with different optimizers (Adam, SGD, RMSProp) and learning configurations to identify the best-performing setup.

⚙️ Training Configuration
Parameter	Details
Encoders	ResNet50
Optimizers	Adam, SGD, RMSProp
Learning Rate (LR)	0.0010 – 0.0100
Weight Decay	0.0001 – 0.0010
Loss Function	Dice Loss + Cross-Entropy (Combo)
Evaluation Metrics	Dice Coefficient, IoU, Pixel Accuracy
📊 Key Results
Model	Optimizer	Pixel Accuracy	Dice	IoU
U-Net (SGD)	0.9824	0.873	0.775	
FPN (RMSProp)	0.9794	0.851	0.741	
PSPNet (Adam)	0.9344	0.822	0.695	
DeepLabV3 (Adam)	0.9663	0.809	0.680	

✅ Best Performing Model:
U-Net (SGD optimizer) achieved the highest Dice = 0.873 and IoU = 0.775, indicating strong segmentation accuracy and generalization.

🧠 Tools & Technologies

Languages: Python

Libraries: PyTorch, NumPy, OpenCV, Matplotlib

Architectures: U-Net, FPN, PSPNet, DeepLabV3

Encoder: ResNet50

Optimizer: RMSProp, Adam, SGD

Environment: Jupyter Notebook

💡 Insights

The U-Net architecture provided the best performance on this dataset, confirming its strength in biomedical segmentation.

RMSProp and SGD delivered more stable convergence compared to Adam for small medical datasets.

The experiment demonstrated that encoder–decoder architectures with residual encoders significantly enhance medical image segmentation quality.
