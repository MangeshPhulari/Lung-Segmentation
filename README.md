# Lung-Segmentation
# Abstract

Lung segmentation from Chest X-ray images is essential for diagnosing and treating pulmonary diseases. This project leverages the U-Net++ architecture for automated lung
segmentation, enhancing accuracy through nested and dense skip pathways that capture fine details. We collected and pre-processed a comprehensive dataset of chest X-rays
and lung masks, employing data augmentation to improve model robustness. The UNet++ model was trained using a combination of Binary Cross-Entropy and Dice Loss
functions, with training conducted on Google Colab using GPU acceleration. 

# Data and task description 

![final-output](https://github.com/user-attachments/assets/408a3933-f2c5-431b-9990-f6e98b6e5ba4)

Dataset consists of collected from public available chest X-Ray (CXR) images. Overall amount of images is 800 meanwhile labeled only 704 of them. Whole dataset was randomly divided into train (0.8 of total) validation (0.1 splited from train) and test parts.

The main task is to implement pixel-wise segmentation on the available data to detect lung area.
Download link on the dataset and model.                               
Dataset: https://drive.google.com/drive/folders/1NC0nT80PNzv0XpYiR5OuHaN5TM8-sF_h                                                
Model: https://drive.google.com/file/d/1-h3W4s1PafEG6WSowWWtor863K1aKbno/view?usp=drive_link

# Evaluation of Segmentation Results

The qualitative evaluation of segmentation results involves visually inspecting the
output of the model to assess the accuracy of the segmentations. This includes
examining whether the model correctly identifies lung regions in the X-ray images and
whether there are any false positives or false negatives in the segmentations.

Some kinds of data augmentation were used: horizontal and vertical shift, minor zoom and padding. All images and masks were resized to 512x512 size before passing the network. Such network configuration outperforms other variations of unet++ without batch norm and pretrained weights on validation dataset so it was chosen for final evaluation.

Networks were trained on a batch of 2 images during 10 epochs.

Evaluation was performed on test dataset, which was not used during training phase. Some you obtained prediction could see on random images below.

![random-image-output](https://github.com/user-attachments/assets/f7bdb888-6701-4645-a320-3971fdf8e23b)

# Final Output

![output](https://github.com/user-attachments/assets/3ac7a230-0a66-41a6-9a18-ab2ca35b3f46)



