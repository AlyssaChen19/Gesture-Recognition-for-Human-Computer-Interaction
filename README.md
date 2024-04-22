# **Gesture Recognition for Human-Computer Interaction**

## **Contributors**
- Yi-Cheng Chung
- Yu-Chin (Alyssa) Chen
- Shuo Ming Kuo
- Ya Chu Hsu

## **Motivation**
Gesture recognition for human-computer interaction harnesses neural network technologies to tackle real-world business challenges, particularly those involving complex data. By employing algorithms and sensors to interpret human gestures as commands, this technology enables users to interact with computers or devices without physical touch, using hand, finger, or body movements. Its applications span various fields, including gaming, virtual reality, robotics, and assistive technology for the disabled, enhancing the intuitiveness and accessibility of device control. Leveraging neural networks in gesture recognition can further advance technology and elevate it to new heights.

## **Problem Statement**
The technology of Gesture Recognition for Human-Computer Interaction has not yet matured, so there are not many successful, well-known, and globally used products. In our project, we aim to utilize neural networks and analyze videos and pictures to predict the accuracy of over 20 different gestures, each comprising 47 videos as inputs. The output will be the gesture classification, which we will use to assess accuracy, in an effort to enhance Gesture Recognition for Human-Computer Interaction and advance the technology.

## **Dataset**
The dataset used in this project is the ChaLearn Gesture Dataset (CGD 2011), collected by ChaLearn in California in 2011. It comprises 50,000 samples stored as AVI files, capturing a wide range of movements using Kinect cameras. Each sample consists of videos displaying color and depth, with frames sized at 240 x 320 pixels. The data originates from recordings by 20 different users and is organized into 500 batches, each containing 100 movements. Movements are further grouped into 47 sequences, with each sequence containing 1 to 5 movements from various small movement sets, totaling over 30 different sets. The dataset includes two main parts: the devel-1-480 archive, containing labeled samples for model building and testing, and the verify-1-20 archive, which lacks labels and serves to validate predictions against real data.

## **Methodology**
Our approach involves defining gesture classifications and preprocessing videos and images for input into our models. We experiment with various network architectures, considering both spatial and temporal features. Our initial models include CNNs, Inflated 3D CNNs, DNNs, RNNs, and ANNs. We conduct hyperparameter tuning by experimenting with different model structures and hyperparameters, such as determining the number of layers and neurons, selecting optimal activation functions, adjusting the learning rate value, or employing more complex callback methods. Finally, we evaluate our results using a variety of metrics, including confusion matrices, ROC curves, AUC, and cross-entropy loss.

