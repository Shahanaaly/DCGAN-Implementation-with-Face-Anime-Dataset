1. To run this code, you must specify exact paths inside the code. The code was initially written based on different websites like GitHub and Reddit. Then, in the final stage, it is optimized by using the Open-AI Canvas to refine and remove unnecessary code and repetitions. 

2. This code is written in a Jupyter notebook/Google Colab notebook, so you need to use Jupyternote Book or Google Colab with Python 3.

3. Necessary Pytorch dependencies are mandatory

4. The code file "DCGAN Optimized Code" contains 9 chunks of codes i.e., 
	
	1. Install Required Libraries
	2. Unzipping Files
	3. Dataset Preprocessing
	4. Creating Dummy Class Folder
	5. Creating Data Loader
	6. Creating Folder for Generated Images
	7. Initialize Model and Optimizers
	8. Initial Run and Test Code Script
	9. Model Training, saving training logs, and saving models at different epochs

5. After running the code, you will have the following folders

	a) Dataset (Initially, the Zipped dataset is unzipped to this folder)
	b) Processed_Dataset (The unzipped Dataset has been preprocessed according to provided guidelines
	c) Test_Generated_Images (A test run has been executed to determine whether the code is running correctly and generating synthetic images)
	d) Generated_Images (All the generated images are stored into this folder)
	e) saved_models (Generator and Discriminator Models are saved at different epochs)
	f) .ipynb_checkpoints folder contains training code and training checkpoints

6. A text file, training.txt contains all the training logs

7. In this github code we just included last two saved models i.e., generator_epoch_50.pth and discriminator_epoch_50.pth as there is problem in establishing a connection with the GitHub and our local machine. Which we will fix in the future.
