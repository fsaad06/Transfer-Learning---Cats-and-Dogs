# 🐱🐶 Cat Dog Classifier Using Transfer Learning

Welcome to the Cat Dog Classifier project! This project utilizes transfer learning to build an efficient and accurate image classifier for cats and dogs using PyTorch.

## 📄 Project Overview

We tested several models pre-trained on ImageNet to build a Cat and Dog Image Classifier. After applying feature extraction to different models, we compared their losses, accuracy, and inference time to select the best model. MobileNet v2 emerged as the most effective in terms of both accuracy and inference time. We also analyzed PyTorch's built-in quantized model.

### Framework Used: **PyTorch**

## 📚 Introduction

Refer to the [PROJ_REPORT.pdf](./PROJ_REPORT.pdf) in the base directory for complete documentation.


## 🛠 Requirements

1. Google Colab Account (Add.: Mounted Drive)
2. Images and labels in `.npy` format.
3. Proper import of all libraries mentioned in the code.

**PyTorch Version:** `1.12.1+cu113`

## 🚀 How It Works

1. **Upload**: Ensure the images and labels (`.npy` format) are uploaded to the working directory.
2. **Preprocessing**: Convert the given image arrays into PNG format for easier handling by PyTorch.
3. **Verification**: Place verification checkpoints often, mainly through visualization.
4. **Flexibility**: The code provides flexibility in compute resources (CPU or GPU).
5. **Transfer Learning**: Train with a huge dataset in advance, then replace the output layer with our purpose. Fine-tuning and feature extraction are the two approaches used here.
6. **Feature Extraction**: Update only the final layer weights to derive predictions. We used part of MobileNet_v2 (pre-trained on ImageNet) as a feature extractor and trained additional new layers for cats and dogs classification.
7. **MobileNet v2**: A 53-layer deep convolutional neural network, known for reduced memory size and inference time.
8. **Saving Model**: Save the trained model in your local directory (designed to save on mounted Drive).
9. **Testing**: Use the saved model for testing on given testing images.
10. **Inference Time**: A small cell calculates inference time.
11. **Additional**: Install `efficientnet_pytorch` and `timm` for EfficientNet_b0 and Inception v3, respectively, every time you use them.

## 🌐 API Configuration

Using APIs as a clean interface between the analytics and the application allows for faster product development and reusability of developed models.

**API Used**: Web-based API named 'Streamlit'.

1. **API Testing**: Designed to test MobileNet v2, ResNet-18, and VGG-16.
2. **Streamlit File**: Create a file named `streamlit.py` in the working directory to prevent bugs.
3. **Local Hosting**: The web page starts to be locally hosted after running the last cell. Click on the provided link, pass through the tunnel page, and access the desired page.

## 📌 Additional Note

If using feature extraction from a pre-trained model, as transfer learning wasn't a condition of the project, and saving the quantized model after feature extraction was possible in PyTorch Framework, then consider moving to the quantized version of the pre-trained model.

## 🐞 Troubleshooting

In case of any problems or bugs, refer to the [PROJ_REPORT.pdf](./PROJ_REPORT.pdf) in the base directory.

Or email me at: saadfarrukh303@gmail.com

---

✨ Happy Coding! ✨
