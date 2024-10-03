# Neural Style Transfer Research Project
Phase 5 Capstone Project for Flatiron school's Data Science Live curriculum
---
# Overview
Neural networks are machine learning models that utilize nodes and connections in order to learn, and are engineered to learn in a similar fashion to our own brains. NNs are often used for typical machine learning tasks such as regression and classification, but it can also be used for more creative and artistic tasks as well. Neural Style Transfer is a machine learning technique that leverages Convolutional Neural Networks to apply the "style" of one image such as a painting or drawing onto another image's "content."

![bird_foam_csg](https://github.com/user-attachments/assets/a3e4889f-0753-42e5-a775-66a95cb7d131)

This repo researches and explores the original Neural Style Transfer algorithm published by Gatys, et. al in their 2016 paper *Image Style Transfer Using Convolutional Neural Networks*. It walks through and applies the [Tensorflow tutorial implementation of NST](https://www.tensorflow.org/tutorials/generative/style_transfer) with extra explanations and a high-level overview of the entire process. It will demonstrate the technique in full with several images of paintings in the public domain and real photos taken with my own smartphone.

# Languages/Packages Used
---
The file `research_notebook.ipynb` is the Jupyter Notebook that this project was implemented in. It uses the following languages, packages and their respective dependencies:

- Python v=3.9.19
- Tensorflow v=2.10.0
  - NOTE: In Tensorflow versions 2.11 and beyond, utilization of the GPU is no longer supported, so this project uses Tensorflow 2.10. If using a later version where only the CPU is utilized, generating images will take much, much longer.
- TensorflowHub v=0.16.1
- NumPy v=1.26.4
- Matplotlib v=3.8.4
- OpenCV v=4.10.0
- PILLOW v=10.4.0
- H5Py v=3.11.0

# NST In Action
---
The process as a whole can be laid out at the conceptual level:
- Select a content image and style image to combine
- Extract the "essence" of both images using a pre-trained neural network
- Create a third image to optimize and extract its "essence" as well
- Calculate the difference between the "essences" of the third image and the content/style images
- Minimize this difference
- The new generated image is a visually appealing combination of the content and style images

Below is a sped up video of the process of optimizing the input image:

https://github.com/user-attachments/assets/0b563b2a-cddc-49d0-8125-13f1e9fed0ef
