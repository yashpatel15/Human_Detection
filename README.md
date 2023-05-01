# HUMAN DETECTION ON CUSTOM DATASET.


-------------------------------------------------------RUN INFERENCE WITH THIS REPOSITORY-------------------------------------------------------

Copy this Github Repository

In the data folder make two folders : train and val
Inside the train folder make two sub-folders images and labels
Inside the val folder make two sub-folders images and labels

After creating folders download the dataset from this link : https://universe.roboflow.com/ds/fGyOZh5K2w?key=kT1q5Z7SRe
Copy the train and test data set and paste in the respective folders in the data folder.

Make conda environment in your local machine, activate it and run the following code in the terminal:

pip install -r requirements.txt
pip install -r requirements_cpu.txt
pip install -r requirements_gpu.txt

I have modify some arguments in the code for CPU Usage only so if you want to train on the custom epochs or workers refer to the Run_On_Original_Repository.txt file in my repository

Now if you want to train the model then only run the following code in your terminal (make sure conda environment is activated):

python3 train.py

it will automatically create this folders and subfolders : Detection/Train/.......many more files
now their will be weights folder and inside it their is best.pt file will be formed you can use that weights file for the detection on your images.
i have used the dataset which I mentioned above so if you want to use the weights file for that dataset download it from this link : https://drive.google.com/drive/folders/1R8D_NFBBpfmq6FYdei66CUNpd6o7iKbd?usp=sharing

Now make folder in this form Detection/Train/weights/ in the main directory to sub directories and then inside this folder add the downloaded weight file.

Now to run inference simply run this code :

python3 detect.py --source image.jpg --no-trace

add image path in place of image.jpg also i have set the confidence to 0.5 if you want to change the confidence then you can change the 171 line of detect.py default = 0.5 change it according to your use case.

