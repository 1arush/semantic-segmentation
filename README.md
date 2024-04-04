# semantic-segmentation

This repository is an application of ConvNets, and performs semantic segmentation on landscape images.

The notebook is well documented, and contains explanations for all the code, as well as some illustrations for the
reader's aid. The notebook uses TensforFlow, and can be made to run in a Colab environment. For simplicity, we will pre-add the
dataset to our drive and later mount it in our notebook. This is also helpful since the size of the dataset is quite large (~570MB).

To achieve this we use the classical U-Net architecture, which is incredible for segmentation tasks. It takes an image as
input and produces an output of the same shape as output, while also managing to retain information. To achieve this, it uses
an encoding phase and a decoding phase (explained in the notebook as well).

<img width="887" alt="unet" src="https://github.com/1arush/semantic-segmentation/assets/105356056/a5edf8e7-2ea9-435a-b167-87862516853f">

A few important points:

- The data organization (within the drive) is as follows:
  - data
    - DataRGB (The raw images of our dataset)
    - DataMask (The mask-labels for each of the images)

- The notebook segments the images into 23 classes. This number is chosen based on the dataset.

- It only trains for 5 epochs, and produces an accuracy of 0.87. Results can be further improved by increasing epoch count.

All the materials (including the entire dataset) used for this notebook can be found at [this folder](https://drive.google.com/drive/folders/1YIwZBome0l4c8bZuhYZnjg00UHiuZhhE?usp=sharing).
