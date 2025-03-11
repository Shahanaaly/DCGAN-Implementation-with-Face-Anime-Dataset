**DCGAN-Implementation-with-Data-Augmentation**

In this assignment, we will build a Generative Adversarial Network (GAN) capable of generating realistic images from a custom Pokeman dataset. After training, GAN will be deployed as a web-based platform where users can generate new images with a  button click.  

**1.	Generative Adversarial Network (GAN)?**
   
Generative Adversarial Network (GAN) [1] entails training two neural networks to compete against each other to create new data from a given training set. For instance, we can generate new data from original data. Data could be in any form, such as images, text, audio, or signal data. As the network suggests, it has two neural networks, and one network is responsible for generating new data from the given input data (and modifying it as much as possible). The other predicting network determines whether the generated data is fake or real. The training of these two networks persists until the prediction network can no longer distinguish fake from original.

**2.	Choosing Dataset, Applying Data Augmentation, and Preprocessing**
We choose the Pokemon Dataset [2] to train the GAN network. The reason for selecting this dataset is that it has a limited number of images, i.e., 1638, which is insufficient for training the network. Therefore, we applied data augmentation techniques [3]. For example, in our case, we apply flipping, rotation, jittering, and affine techniques. A total of 4914 synthetic (augmented) images were generated. In terms of preprocessing, we resize it to 64x64 and further normalize it to range [-1, 1] for stable GAN training. The same preprocessing techniques. Next, we combine both the original and augmented images into a combined dataset, i.e., a preprocessed dataset with a total of 6552 images (1,638+4,914). Finally, create a DataLoader which prepare the dataset for efficient training.

**3.	Implementation of Deep Convolutional GAN (DCGAN)**
DCGAN was implemented successfully according to the requirements mentioned in the assignment description. The DCGAN code was adopted and modified (according to our custom dataset ) from the given Github repository [4]. 

•	Used transposed convolutions at the Generator side

•	Used ReLU activation and Tanh for output at the Discriminator side

•	Used convolutions, batch normalization, and Leaky ReLU in the Training phase

•	Uses Binary Cross-Entropy Loss 

•	Optimized with Adam optimizer

•	Trains for 50 epochs

•	Saves generated images at different epochs

**References**
1.	Goodfellow, Ian, Jean Pouget-Abadie, Mehdi Mirza, Bing Xu, David Warde-Farley, Sherjil Ozair, Aaron Courville, and Yoshua Bengio. "Generative adversarial nets." Advances in neural information processing systems 27 (2014).
2.	https://www.kaggle.com/datasets/kvpratama/pokemon-images-dataset 
3.	 Perez, L., & Wang, J. (2017). The effectiveness of data augmentation in image classification using deep learning. arXiv preprint arXiv:1712.04621.
4.	https://github.com/eriklindernoren/PyTorch-GAN/tree/master



