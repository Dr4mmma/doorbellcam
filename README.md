# Doorbell Security Camera System

Using Python Deep Learning algorithms in order to monitor visitors and classify them using a doorbell camera based on Image Recognition.





<p align="center" style="margin-top=100px">
  <img src="https://i.ibb.co/rQybBcT/Ring-Doorbell-700x442-removebg-preview.png">
</p>



# Credits 

| Project | License  | 
| :---:   | :-: | 
| [face_recognition](https://github.com/ageitgey/face_recognition#python-code-examples) | [License](https://github.com/ageitgey/face_recognition#python-code-examples) |
| [Adam Geitgey](https://medium.com/@ageitgey/build-a-hardware-based-face-recognition-system-for-150-with-the-nvidia-jetson-nano-and-python-a25cb8c891fd) | [License](https://medium.com/@ageitgey/build-a-hardware-based-face-recognition-system-for-150-with-the-nvidia-jetson-nano-and-python-a25cb8c891fd) |


# Installation

## Hardware
* OS: Ubuntu 16.04 (at least) or Windows 10 (Maybe MacOS as well).
* Runs on both CPU

## Software
* Download and Install 64-bit Anaconda 3
  * While installing Anaconda make sure that you check both options:
    Add Anaconda to my PATH environment variable
    Register Anaconda as my default Python
    Add Anaconda to System PATH and make it default Python
* Create Virtual Environment
  * Open the command prompt and execute the following command:
  
    `conda create --name opencv-env python=3.6`
* Activate the environment and installing packages
  * Activate virtual environment (See how the (opencv-env) appears before the prompt after this command): 
  
    `activate opencv-env`
  * Install OpenCV and other important packages continuing from the above prompt, execute the following commands:
  
    `pip install numpy scipy matplotlib scikit-learn jupyter`
    
    `pip install opencv-contrib-python`
    
    `python -m pip install https://files.pythonhosted.org/packages/0e/ce/f8a3cff33ac03a8219768f0694c5d703c8e037e6aba2e865f9bae22ed63c/dlib-19.8.1-cp36-cp36m win_amd64.whl#sha256=794994fa2c54e7776659fddb148363a5556468a6d5d46be8dad311722d54bfcf`
    
* Test your installation
  * Open the python prompt on the command line by typing python on the command prompt and then execute the following:
  
    `import cv2`
    
    `cv2.__version__`
    
     `import dlib`
     
     `dlib.__version__`
     
* Install the face recognition module that this system is based on:

     `pip install face_recognition`
* Other packages may be needed to get installed, but you're almost there!

# How to use it (inluding brief summary of what you see):

## 1. Running the project:
* Execute the following command to run the project:

  `python doorbellcam.py`
  
  
## 2. Face detection test:
By using the following module:
  * [face_recognition](https://github.com/ageitgey/face_recognition#python-code-examples)

  
Which was already done in the following project: [Hardware Security System](https://medium.com/@ageitgey/build-a-hardware-based-face-recognition-system-for-150-with-the-nvidia-jetson-nano-and-python-a25cb8c891fd), you will recognize the following appearing on your screen:

![picture alt](https://i.ibb.co/F63c9XZ/doorbellcam-pic.png)

## 3. Determining if the visitor is a new visitor or not:
This was done by saving data of who approaches the door's camera into a .dat file.

If the person is a new visitor, the following will appear:

<p align="center">
  <img src="https://i.ibb.co/X7hTH2X/1st.png">
</p>

If the person has visited the door before, the following will appear:

<p align="center">
  <img src="https://i.ibb.co/TqptQHh/2nd.png">
</p>

## 4. Classifying the behavior of strange visitors:
This was done after making a study that resulted in two acts a strange person might do:

1. If a visitor does not ring the bell for 60 seconds, an alarm will go on that warns the people inside this property.

<p align="center">
  <img src="https://i.ibb.co/ypL2zCF/Screenshot-1.jpg">
</p>

2. If a visitor does not ring the bell for 120 seconds, an alarm will go on that warns the people inside this property, and the system will send a whatsapp message using Twillio with the strange visitor picture with a warning message.

<p align="center">
  <img src="https://i.ibb.co/T02B9sP/owl.png">
</p>

## 5. Implementation:
This project will be ran on Jetson nano/xavier, as it is a mini computer that was made for AI projects.

<p align="center">
  <img src="https://elinux.org/images/9/93/Jetson-Xavier-NX-DevKit-Module.jpg">
</p>

###### Picture belongs to: [elinux](https://elinux.org/Jetson_Xavier_NX)

# Video
Video is coming soon!!!!

# Final thoughts
I would consider this project finished, but there will be minor modifications to data gathered and how alarm system goes on in order to assure high accuracy.
The final product will be available soon, and hopefully I can get a commercial product available at very cheap price.
I would love the opportunity to have a talk with a production company that can help me to get to a commercial product.

Thank you for your time, this code is available for any developer that wants to go further with this project.
Contact me for any further details at: mohammad.tayseer.comn@gmail.com

# Licenses
  * [face_recognition](https://github.com/ageitgey/face_recognition#python-code-examples)
  * [Adam Geitgey](https://medium.com/@ageitgey/build-a-hardware-based-face-recognition-system-for-150-with-the-nvidia-jetson-nano-and-python-a25cb8c891fd)

