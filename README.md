# **Gesture Recognition for Human-Computer Interaction**

## **Contributors**
- Yi-Cheng Chung
- Yu-Chin (Alyssa) Chen
- Shuo Ming Kuo
- Ya Chu Hsu

## **Motivation**
Neural network technologies can be beneficial in finding innovative solutions to real-world business challenges, especially those involving complex data. Gesture recognition for human-computer interaction entails the use of algorithms and sensors to interpret human gestures as commands. This technology enables users to interact with computers or devices without physical touch, utilizing movements of the hands, fingers, or even the entire body. It has been applied in various fields such as gaming, virtual reality, robotics, and assistive technology for the disabled, thereby enhancing the intuitiveness and accessibility of device control. Neural networks in Gesture Recognition for Human-Computer Interaction can further enhance technology and propel it to a higher level.

## **Problem Statement**
The technology of Gesture Recognition for Human-Computer Interaction has not yet matured, so there are not many successful, well-known, and globally used products. In our project, we aim to utilize neural networks and analyze videos and pictures to predict the accuracy of over 20 different gestures, each comprising 47 videos as inputs. The output will be the gesture classification, which we will use to assess accuracy, in an effort to enhance Gesture Recognition for Human-Computer Interaction and advance the technology.

## **Dataset**
This dataset (ChaLearn) contains a wide range of movements recorded using Kinect cameras, which includes 50,000 samples stored as AVI files. These samples consist of videos showing color and depth, with each frame being 240 x 320 pixels. The data comes from recordings made by 20 different users and is organized into 500 batches, each containing 100 movements. Within these groups, movements are grouped into 47 sequences, each sequence having 1 to 5 movements from various small movement sets, totaling over 30 different sets. 
Additionally, the dataset has two main parts.First, the devel-1-480 archive has labeled samples used to build and test the model. Second, verify that the 1-20 archives have no labels, used to check how well the predictions match the real data. 

## **Methodology**
- **Data Preparation**: Our initial step involved selecting a representative subset of the labeled samples from the ChaLearn Gesture Dataset. This strategic choice helped us not only in reducing computational costs but also in streamlining the development process. For a focused and effective analysis, we specifically utilized test videos depicting a single gesture movement. We processed these videos by segmenting them into individual frames, captured at intervals of 0.05 seconds. This method of frame extraction, which yielded between 4 to 10 images per video, was crucial for capturing essential temporal nuances and maintaining a standardized input format for model training and evaluation.

- **Frame Rate and Temporal Resolution Adjustments**: In our endeavor to refine the model's accuracy and efficiency, we methodically reduced the number of distinct gesture labels from 478 to 20. We also enhanced our frame extraction precision by shortening the time interval between frames from 0.5 seconds to 0.05 seconds. These adjustments allowed us to capture more detailed temporal dynamics without compromising processing speed.

- **Model Architecture and Training**: For gesture recognition, we utilized Convolutional Neural Networks (CNNs), well-known for their effectiveness in image analysis. Additionally, we experimented with the VGG pre-trained model due to its advantages in various computer vision tasks, including gesture recognition. Trained on extensive datasets like ImageNet, VGG possesses a wide array of learned features that can be used for transfer learning. By leveraging VGG's hierarchical representations on generic image data, practitioners can benefit from its ability to extract detailed and relevant features for gesture recognition.

- **Data Augmentation and Hyperparameter Optimization**: To further improve the model's robustness and generalization ability, we applied various data augmentation techniques such as rotation, zoom, and horizontal flipping. These transformations help the model become invariant to common variations in new video data. Additionally, extensive hyperparameter tuning was performed to optimize the network's architecture and training process. We experimented with different settings for dropout rates, activation functions including ReLU, Leaky ReLU and ELU , batch sizes, and learning rates. Employing a grid search approach, we methodically explored numerous combinations of these parameters to find the most effective settings for our model. By implementing these methods, we aim to significantly advance the capabilities of gesture recognition systems, enhancing their accuracy and applicability in real-world human-computer interaction scenarios.

## **Communicating Results** 
Our hyperparameter tuning efforts, guided by systematic grid search strategies, have led to valuable insights that have greatly improved our model's ability to predict correctly. We explored a variety of learning rates, batch sizes, and dropout rates in detail. We tested learning rates of 0.01 and 0.001, batch sizes of 32 and 64, along with dropout rates of 0.2 and 0.3. This thorough exploration was crucial in determining how the model reacts under different settings.

Our results indicate that the learning rate was the most influential parameter, followed by batch size and dropout rate. The results of this careful process are clearly demonstrated in our parallel coordinates plot. The model that stands out for its performance under different hyperparameter settings used a batch size of 64, a dropout rate of 0.2, and a learning rate of 0.001. (Figure 1.) The results are highlighted by the orange line on the plot, showing a relatively high F1 score and a test accuracy of 51.56%. 

Moreover, our analysis of the training process, shown through epoch progression charts, reveals the learning stability over time. (Figure 2.) The training accuracy and loss graphs show that the model is effectively learning, with the lines coming together toward higher accuracy and reduced loss as training progresses. The test accuracy and F1 score, when viewed alongside the training graphs, show the model’s poor performance. A low F1 score might indicate an imbalance, so we re-examine the distribution of the test dataset and find that some labels have four times more testing images than the others.

Lastly, the confusion matrix (Figure 3.) provides a detailed look at the model's ability to predict across various gesture classes. The results clearly show that our model tends to predict most of the images in classes 11, 3 and 9, which demonstrates a mis-classification. We look back into the original dataset and realize that gestures in these classes contain moves that are more general, such as waving hands or moving hands upwards and downwards. This can potentially affect the model to mis-classify other classes if they also contain similar images.

In summary, our project represents a significant advance in the field of gesture recognition. The improvements in accuracy and our detailed understanding of how hyperparameters affect the model establish a firm foundation for future enhancements in this intriguing aspect of human-computer interaction.


## **Conclusion**
Our project has made important progress in the field of gesture recognition with the use of neural networks. By trying different data preparation methods, various neural network models, and extensive hyperparameter tuning, we have managed to improve our model's test accuracy from 6% to an impressive 52%. This improvement underscores the potential of neural networks to interpret human gestures, which is a significant step towards enhancing human-computer interaction.

Yet, we must consider the possibility that our model may be biased towards certain visual elements in the data, rather than the gestures themselves. This possibility calls attention to the importance of ongoing scrutiny in the training processes of machine learning models to ensure they learn to recognize what they are supposed to.

Future work should explore incorporating video-based inputs into our models. The richness of video data, capturing the full sequence of human motion, could provide a more comprehensive understanding of gestures over time. This approach could potentially increase the accuracy and reliability of gesture recognition systems.

It is our hope that subsequent research will continue to build on our findings, using video data to capture the fluidity and complexity of human gestures. Such advancements could lead to significant improvements in natural and intuitive human-computer interactions, paving the way for more responsive and adaptable technology.

## **Reference**
- https://keras.io/api/layers/activation_layers/elu/
- https://keras.io/api/layers/activation_layers/leaky_relu/
- https://www.kaggle.com/code/kasana/image-classification-using-keras-cnn
- https://huggingface.co/timm/vgg16.tv_in1k
- https://keras.io/api/applications/vgg/
- https://docs.clarifai.com/tutorials/how-to-evaluate-an-image-classification-model/

## **Use of AI Tools:**
Using ChatGpt to refine the wording parts and to debug code.
