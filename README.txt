# ============================================================================
# Name        : main.ipynb				                               // Name : Muhammad Saad Farrukh						               
# Copyright   : (c) Reserved					                               (Last updated: 2012-09-05 at 23:42:01)
# Description : Cat Dog Classifier Using Transfer Learning 
# ============================================================================

>>>>>>> Refer to the 'PROJ_REPORT.pdf' in base directory for complete documentation. <<<<<<<  

INTRODUCTION
------------
    We tested several models, pre-trained on ImageNet, to build a PyTorch Cat and Dog Image Classifier using Transfer Learning. After applying feature 
extraction to different models, we compared their losses, accuracy and inference time to select the best model. We found MobileNet v2 to be most effective 
with respect to both accuracy and Inference Time. We also performed analysis of PyTorch's built-in Quantized Model. 

                                         --------- FrameWork Used : PyTorch ---------  

CODES LINK
----------
MAJOR: >> main.py :  https://colab.research.google.com/drive/1r1wyeKY7syziB30ameLnKhVn4NVnPHDP?usp=sharing
       >> API :      https://colab.research.google.com/drive/1AhyE52cDKASxaB4nZV1ZmL34Ax9jLpfm?usp=sharing

ADDITIONAL:  >> ResNet-18 :            https://colab.research.google.com/drive/1Q8xmaIMAnMW1DMzUQx0YV9SH4Bk9PFG4?usp=sharing
             >> ResNet-50 :            https://colab.research.google.com/drive/1HJYMstRKOL5z2nPvvSl_gvRNqMqjjcBC?usp=sharing
             >> VGG-16    :            https://colab.research.google.com/drive/1cwLprw_0RjEzmDrBWkOeTd9GbMpjaQpj?usp=sharing
             >> EfficientNet B0 :      https://colab.research.google.com/drive/1zNzqegcTSfn2ELH9s0A0eo9bzD-1w18k?usp=sharing
             >> Inception v3    :      https://colab.research.google.com/drive/1lpbZhdlDQz6HidKGFpU6cRZ6ynonpEUH?usp=sharing
             >> Xception  :            https://colab.research.google.com/drive/1FuRdEHmSCZoz9urTyA4RXkTh18Mv0B_7?usp=sharing
             >> Quantized ResNet-18 :  https://colab.research.google.com/drive/12xkWARk20ad8Yyu6oePJsWZzRlRfKuXZ?usp=sharing


REQUIREMENTS
------------
1. Google Colab Account (Add.: Mounted Drive)
2. Given Images and Labels in the form of .npy format.
3. Properly Import of all the Libraries, mentioned in the code.

>> The latest PyTorch's version upon which we worked is '1.12.1+cu113'


HOW IT WORKS?
-------------
-> UPLOAD:             Make sure to upload the given Images and Labels (.npy format) in the working directory.

-> PREPROCESSING:      Since PyTorch is more comfortable to handle on Image dataset, so given Image arrays have been converted into PNG format.

-> VERIFICATION:       Verification check-points have been placed often, mainly in form of Visualization.

-> FLEXIBILITY:        Code has been designed to provide flexibility in compute resources (CPU or GPU).

-> TRANSFER LEARNING:  A sort of learning method that train with huge dataset in advance, then replace the output layer with our purpose. 
                       Fine-tuning and Feature Extraction are two different approaches used here.

-> FEATURE EXTRACTION: Only updates the final layer weights from which we derive predictions.
    
     >> We used part of MobileNet_v2 (pre trained on ImageNet) as a feature extractor, and train additional new layers to perform the cats 
       and dogs classification task <<

-> MOBILENET v2:       A 53 layers deep CONV. neural network, known to have reduced memory size and inference time.

-> SAVING MODEL:       After training, model becomes saved on your local directory. (Here it's designed to save on mounted Drive)

-> TESTING:            Saved model is then called to be used for testing on given Testing Images.

-> INFERENCE TIME:     Small cell has also been designed to calculate Inference Time.

-> ADDITIONAL:         Make sure to install 'efficientnet_pytorch' and 'timm' for EfficientNet_b0 and Inception v3 respectively, everytime you use them. 


API CONFIGURATION
-----------------
    Using APIs as a clean interface between the analytics and the application that makes use of them allows for faster product development and reusability 
of developed models in multiple applications.
    The used API is web-based API named 'Streamlit'.

-> API has been designed to test three models; MobileNet v2, ResNet-18 and VGG-16.

-> Make sure to create file name 'streamlit.py' in working directory, in order to prevent bugs.

-> Web-page starts to be local hosted, after you run the last cell.

-> Click on the provided link, Pass through the Tunnel page and there you go to your desired page.


ADDITIONAL NOTE
---------------
    If 
      1. Using Feature Extraction from Pre-Trained Model, as Transfer Learning wasn't the condition of Project
      2. Saving Quantized model after Feature Extraction, was possible in PyTorch FrameWork
  
    then, surely move to Quantized version of Pre-Trained Model.


TROUBLESHOOTING
---------------
    In case of facing any problem or bug, refer to 'PROJ_REPORT.pdf' in base directory.
   
( >> or email me at saadfarrukh303@gmail.com )

                          **************************************************************************************************