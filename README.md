<div align="center">
<h1 align="center">
<br>ACTION DETECTION-OPENVINO-INTELDEVCLOUD</h1>

</div>

---

## 📖 Table of Contents
- [📍Project overview](#-overview)
- [📍What is oneapi](#-features)
- [📍IntelDevCloud](#-inteldevCloud)
- [📍OPENVINO](#modules)
- [📍Runtime execution](#-Runtime-execution)
- [📍Repository Structure](#-repository-structure)
- [🚀 Getting Started](#-getting-started)
    - [🔧 Installation](#-installation)
    - [🤖 Running ActionDetection-openvino-inteldevCloud](#-running-ActionDetection-openvino-inteldevCloud)


---

## 📍Project overview

   This project focuses on Human Activity Recognition (HAR) by leveraging the UCF101 dataset. HAR is achieved through the extraction of features using OpenCV, followed by training using ConvLSTM3D. The ConvLSTM3D model is particularly well-suited for time series data, making it ideal for processing video and audio sequences.

In our initial model, we achieved a training accuracy of 56% when using 60% of the total dataset. We are actively working to further enhance this accuracy score, with the goal of improving the model's performance.

One notable aspect of our project is the evaluation of runtime execution. We test the trained model using both TensorFlow and Intel OpenVINO IR models. Interestingly, OpenVINO outperforms TensorFlow in terms of runtime execution, completing the task in half the time.

Our commitment to ongoing improvements and the exploration of different frameworks allows us to continually enhance the project's capabilities and offer an effective solution for human activity recognition.

---

## 📍Project overview
    In this project, we initially trained and executed our model without leveraging Intel's optimized libraries and the oneAPI toolkit. While our accuracy was commendable, our system's efficiency left room for improvement.Upon integrating the Intel-optimized TensorFlow model and executing it using OpenVINO IR models, we achieved the same level of accuracy while drastically improving efficiency. This optimization reduced runtime and effectively optimized the hardware load during training.An integral part of Completing this project is the use of the Intel oneAPI cloud, which offered a fast and well-optimized environment for our project. We trained our model using approximately 9000 videos, each comprising 25 frames, and the cloud infrastructure proved to be both efficient and responsive.Furthermore, Intel's optimized version of the scikit-learn library (scikit-learn-intelx) played a role in our project which is used it efficiently split our dataset into training and testing data." 
____
## 📍 What is OneAPI

   OneAPI is an open, standards-based, cross-architecture programming model developed by the oneAPI consortium, which is led by Intel. This initiative aims to simplify the development of high-performance, heterogeneous applications that can run on a variety of hardware architectures, including CPUs, GPUs, FPGAs, and other accelerators. It's designed to address the challenges of modern computing, where hardware diversity is increasing, and software needs to be optimized for different types of processors.

   <img src='https://www.intel.com/content/dam/developer/articles/technical/oneapi-what-is-it/f1-oneapi-specification-stack.png' />
<a href='https://www.intel.com/content/www/us/en/developer/tools/oneapi/toolkits.html'>Oneapi toolkit:link:</a>



---

## 📍Intel®DevCloud

Intel® DevCloud for oneAPI is a cloud-based development platform provided by Intel® that allows developers to access a diverse range of Intel hardware architectures for testing and optimizing their software applications using the oneAPI programming model. This cloud-based environment is particularly useful for those who want to explore the capabilities of oneAPI, but may not have access to the required hardware locally or want to leverage the cloud's scalability and flexibility.

<a href='https://consumer.intel.com/intelcorpb2c.onmicrosoft.com/B2C_1A_UnifiedLogin_SISU_CML_SAML/generic/login?entityId=www.intel.com&ui_locales=en'> link for intel dev cloud 🔗</a>

---


## 📍OPENVINO

The OpenVINO™ toolkit enables you to optimize a deep learning model from almost any framework and deploy it with best-in-class performance on a range of Intel® processors and other hardware platforms.It is an open-source toolkit developed by Intel that helps accelerate the deployment of computer vision and various ML,DL libraires(Tensorflow and PyTorch) on various Intel hardware platforms. It is designed to optimize and run neural network models with high performance and efficiency, making it an essential tool for developers working on applications such as object detection, image segmentation, facial recognition, and more.

<a href='https://docs.openvino.ai/2023.0/openvino_docs_install_guides_overview.html?ENVIRONMENT=DEV_TOOLS&OP_SYSTEM=WINDOWS&VERSION=v_2023_0_2&DISTRIBUTION=PIP'>🔗Getting started with OPENVINO</a>

---
### 📍Runtime execution

   Upon testing both the TensorFlow model and the OpenVINO IR model using the same test data, it was observed that the OpenVINO model outperformed TensorFlow in terms of runtime execution. The OpenVINO model exhibited notably superior performance, completing the task in significantly less time, demonstrating its efficiency for real-time execution

<h4>Tensorflow runtime= 81.01sec</h4>

<img src='https://drive.google.com/uc?export=view&id=1uO8T1vJbHx9n1_U3YXKHFBahq0qHuORF' alt='Tensorflowruntime.png'/>

<h4>OPENVINO IR runtime = 45.24Sec</h4>
<img src='https://drive.google.com/uc?export=view&id=1pFT8bcOLWCKLOrw5nq0bMk4ISoTfdVeT' alt='opevinoIRruntime.png'/>




---



## 📂 Repository Structure

```sh
└── ActionDetection-openvino-inteldevCloud/
    ├── intelfinal.ipynb
    ├── model/
    │   ├── action.tf/
    │   │   ├── fingerprint.pb
    │   │   ├── keras_metadata.pb
    │   │   ├── saved_model.pb
    │   │   └── variables/
    │   ├── model.bin
    ├── output/
    └── test_video/

```

---




## 🚀 Getting Started

***Dependencies***

Dependencies for the project:  
`- ℹ️ Intel_extension_for_tensorflow`

`- ℹ️ OPENVINO`

`- ℹ️ OpenCV`

`- ℹ️ Tensorflow`

`- ℹ️ Sklearn(intel optimsed version of scikit-learn libraires)`

`- ℹ️ Pytube`

`- ℹ️ Moviepy`

### 🔧 Installation

1. Clone the ActionDetection-openvino-inteldevCloud repository:
```sh
git clone https://github.com/Adhi2624/ActionDetection-openvino-inteldevCloud
```

2. Change to the project directory:
```sh
cd ActionDetection-openvino-inteldevCloud
```
3. Create a virtualenv
```sh
python -m venv intelenv
source intelenv/bin/activate
```


4. Install the dependencies:
```sh
pip install openvino-dev==2023.0.2 Intel_extension_for_tensorflow[cpu]scikit-learn-intelex opendatasets opencv-contrib-python Tensorflow==2.13 pytube moviepy
```

### 🤖 Running ActionDetection-openvino-inteldevCloud
You can run this on your local machine by installing the above dependencies otherwise try oneAPI dev cloud or intel cloud console which is free cloud platform from intel with preloaded Oneapi toolkit and Intel® optimized libraires
```sh
jupyter nbconvert --execute notebook.ipynb
```
---





