# Neural Networks History Primer and Utilizing  Convolutional Architectures

Here's a 2-part talk I gave due to the massive progress and interest in deep learning.  
<br>
**Part I: A Comprehensive Primer of the History of Neural Networks:**
Starting from the inkling then known as Cybernetics of the 1940s, we delve into neural networks reborn as Connectionism in the late 1980s. Then, we jump to the current rebranding of neural nets as deep learning from 2006 and onwards. We talk about the advances made in hardware as well as fundamental algorithmic improvements--from the Canadians led by Geoff Hinton as well to the British with the Visual Geometry Group.  
<br>  
**Part II: A Walk Through Convolutional Architectures over the Years:**
Starting with an interesting challenge on 
[Kaggle's Galaxy Zoo competition](https://www.kaggle.com/c/galaxy-zoo-the-galaxy-challenge), the goal is to classify images for a multi-class dataset of relatively large color images.  
We start off with Yann LeCun's LeNet (1998), built for reading MNIST-like digits on checks for ATM machines. Then, we implement the 2012 ImageNet winner, AlexNet, where we train the convolutional filters from scratch. Lastly, we take 2014 ImageNet runner-up, VGG16, where we modify the architecture to include batch normalization. From an implementation standpoint, we separate the convolutional layers from the fully connected layers--the reason being that the freeze the weights on the convolutional layers and are only interested in training the weights on the dense layers. In addition, we apply data augmentation to the raw images (sheering, rotation, translation, color intensity) and feedforward these augmented images into the convolutional model 1 time. Then, we train the fully connected model for several epochs.  
**BONUS: PCA + Random Forest**
Instead of solely using deep learning, we used PCA to reduce a high-dimensional input to a more tenable size (150k relatively sparse features -> 100 compressed features). Then, we grid-search Random Forest using Stratified K-Fold Validation to reduce overfitting. The results were actually comparable to the neural nets!  

**LESSONS LEARNED:**
1. Don't be a hero--use pretrained net!  
2. Historical convolutional architectures actually perform pretty well
3. PCA + RF are a good combo--performance is comparable to deep learning models  
4. Neural net = Infinitely flexible function + All-purpose parameter fitting (Backprop) + Fast and scalable (GPU)  


### Thank you!

![alt text](https://upload.wikimedia.org/wikipedia/commons/7/74/Ngc5194.jpg "Galaxy")

