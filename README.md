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
Before starting the analysis, we selected a representative subset from the labeled samples within the dataset. This strategic choice not only addresses computational limitations but also facilitates a more efficient development process. For this analysis, we opted for test videos from the test set that feature only one  movement. First, we broke down the videos into individual frames, with each frame captured every 0.5 seconds (resulting in 4-10 images for each video). This frame extraction method allows us to capture critical temporal nuances while maintaining a standardized input format required for subsequent model evaluation. 


In our pursuit of accuracy enhancement, we progressively reduced the frame rate from 50 to 5 files, resulting in a corresponding decrease in the number of gestures or labels from 478 to 46. Furthermore, we reduced the time interval per frame from 0.5 to 0.05 seconds, thereby capturing finer temporal details while maintaining efficiency.


Following the data preprocessing stage, we proceeded with the utilization of Convolutional Neural Networks (CNNs) for our analysis. CNNs are widely acknowledged for their efficacy in image recognition tasks, making them a natural choice for our objective of gesture recognition. Specifically, we leveraged a variant of CNN known as Convolutional Recurrent Neural Networks (CRNNs) to account for the temporal aspect inherent in video data. By integrating convolutional layers for spatial feature extraction and recurrent layers for capturing temporal dependencies, CRNNs offer a comprehensive solution suited to our task. 


To augment the data and enhance model robustness, we applied techniques such as rotation, zoom, and horizontal flip. Additionally, we conducted extensive hyperparameter tuning, focusing on dropout layers, activation functions (ReLU / Leaky ReLU), batch size, and learning rate. Employing grid search methodology, we systematically explored various parameter combinations to optimize the model's performance.


