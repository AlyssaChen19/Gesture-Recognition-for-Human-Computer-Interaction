# Gesture-Recognition-for-Human-Computer-Interaction

Contributors: Yi-Cheng Chung, Yu-Chin (Alyssa) Chen, Shuo Ming Kuo, Ya Chu Hsu

Motivation: 
Neural network technologies can be beneficial in finding innovative solutions to real-world business challenges, especially those involving complex data. Gesture recognition for human-computer interaction entails the use of algorithms and sensors to interpret human gestures as commands. This technology enables users to interact with computers or devices without physical touch, utilizing movements of the hands, fingers, or even the entire body. It has been applied in various fields such as gaming, virtual reality, robotics, and assistive technology for the disabled, thereby enhancing the intuitiveness and accessibility of device control. Neural networks in Gesture Recognition for Human-Computer Interaction can further enhance technology and propel it to a higher level.




Dataset: 
This dataset (ChaLearn Gesture Dataset (CGD 2011), ChaLearn, California, 2011) contains a wide range of movements recorded using Kinect cameras, which includes 50,000 samples stored as AVI files. These samples consist of videos showing color and depth, with each frame being 240 x 320 pixels. The data comes from recordings made by 20 different users and is organized into 500 batches, each containing 100 movements. Within these groups, movements are grouped into 47 sequences, each sequence having 1 to 5 movements from various small movement sets, totaling over 30 different sets. 
Additionally, the dataset has two main parts.First, the devel-1-480 archive has labeled samples used to build and test the model. Second, verify that the 1-20 archives have no labels, used to check how well the predictions match the real data.


Methodology:
We will focus on defining gesture classifications and preprocessing videos and images for input into our models. We will experiment with different network architectures, considering both spatial and temporal features.  First we will start off by building different models such as CNNs, Inflated 3D CNNs, DNNs, RNNs and ANNs. Furthermore, we will apply hyper-parameter tuning by experimenting with different model structures and hyper-parameters in these models, including determining the number of layers and neurons, selecting optimal activation functions, adjusting learning rate value or adding more complex callback methods. Finally we will evaluate our results by a variety of metrics such as confusion matrix, ROC curve and AUC or cross-entropy loss.
