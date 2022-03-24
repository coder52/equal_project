[//]: # (Image References)

[image1]: ./assets/folders.JPG "Folder Design"
[image2]: ./assets/run_lab1.JPG "Lab CNN"

# Flower Irrigation System with Deep Learning 

This Project is part of the IoT project at the Hochschule Kaiserslautern. The aim of this part of the project is to create a system that can control and decide the irrigation work of houseplants by using artificial intelligence (Deep Learning and Dens Net). The images required for training CNN to run the project and the .csv file required for training Dens Net are not provided here. 

**Follow the instruction below to run the project**

1. You can run the project with Anaconda the easiest. So download Anaconda or miniconda.

2. You can download the requirements with the help of the **environment.yaml** file.

    - open anaconda prompt.
    - go to the directory where the environment.yaml file is.
    - write 'conda env create -f environment.yaml' command. 
    - click 'y' when y/n has been seen
    - write 'conda activate equal' command when installation finish is
    - if you're seeing 'equal' on the head of the directory in the command prompt you are ready for the next step
    
3. Now enter the `Jupyter Notebook` command at the command prompt

4. Run the `Laboratory for Plant Thirst Classification with Transfer Learning.ipynb` file on the opened browser.

    * A new browser tab will open. In order for the codes in this tab to work, there must be train and test images in a file called 'flowers'. 
    
        ![Folder Design][image1]
        
    * After filling the files with appropriate pictures, run the codes. 
    
        ![Lab CNN][image2]
        
    * If you have enough data (min. 1000 pictures totaly), the test accuracy can easily pass 95%. Model parameters are saved as .pt file. In the last part of our project, we will also use the first artificial intelligence to define the state of plants (0: good, 1: dehydrated) with the data we obtained as a result of training.
    
5. Now let's open the `Laboratory for Watering Decision with Dens Neural Network.ipynb` file to train the second artificial intelligence and run the codes. But you need `temporary_data_.csv` and `Bewässerungszeiten-Datensatz.csv` files for the codes to work properly. The `temporary_data_.csv` file is a completely hand-created file and is required for normalization of data when performing manual testing and using the model. At the same time, new data that will occur during the use of this model are stored in this file. You will find this file in our repo. But the file named `Bewässerungszeiten-Datensatz.csv` which is necessary to train our model will need to be created and saved by the user. 

6. If the files are ready, run the Notebook with the 'Restart & Run All' option under the Kernel as you did in the previous Jupyter Notebook. At the end of the training, the model weights will be saved for later use.

7. Now that we have trained both AIs, we can run our project. For this, let's open the `Run The Project.ipynb` file. This time, I recommend that you run each cell one by one on the Notebook one by one (Shift+Enter). So you can progress by testing each stage.