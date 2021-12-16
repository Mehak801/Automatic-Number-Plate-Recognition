# Automatic Number Plate Recognition

We are trying to leverage Python Tensorflow Object Detection to be able to detect license plates using Kaggle data and test it on data acquired from Delhi traffic police by scrapping  twitter images.
This could be used as a part of a broader system. In extension to this we are trying to convert the images that we are getting in text format using different OCR systems. 

# Project Setup Walkthrough

## Steps
<br />
<b>Step 1.</b> Clone this repository: https://github.com/Mehak801/Automatic-Number-Plate-Recognition.git
<br/><br/>
<b>Step 2.</b> Create a new virtual environment 
<pre>
python -m venv anprsys
</pre> 
<br/>
<b>Step 3.</b> Activate your virtual environment
<pre>
source tfod/bin/activate # Linux
.\tfod\Scripts\activate # Windows 
</pre>
<br/>
<b>Step 4.</b> Install dependencies and add virtual environment to the Python Kernel
<pre>
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=anprsys
</pre>
<br/>
<b>Step 5.</b> Collect images using the Notebook <a href="https://www.kaggle.com/andrewmvd/car-plate-detection">Kaggle train data</a> - ensure you change the kernel to the virtual environment

<br/>
<b>Step 6.</b> Manually divide collected images into two folders train and test. Add kaggle data to train folder with annotations and scrapped twitter data to test folder.<br/>
<em>TO GATHER TEST DATA RUN THE "scrapping_of_twitter_data.ipynb" FILE</em></br>
\ANPR\Tensorflow\workspace\images\train<br />
\ANPR\Tensorflow\workspace\images\test
<br/><br/>
<b>Step 7.</b> Begin training process by opening <a href="https://github.com/Mehak801/Automatic-Number-Plate-Recognition/blob/master/Training_and_Detection.ipynb">Training and Detection.ipynb</a>, this notebook will walk you through installing Tensorflow Object Detection, making detections, saving and exporting your model. 
<br /><br/>
<b>Step 8.</b> During this process the Notebook will install Tensorflow Object Detection. You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK.  
<img src="https://i.imgur.com/FSQFo16.png">

<br /> <br/>
<b>Step 9.</b> Once you get to step 6. Train the model, inside of the notebook, you may choose to train the model from within the notebook. I have noticed however that training inside of a separate terminal on a Windows machine you're able to display live loss metrics. 
<img src="https://i.imgur.com/K0wLO57.png"> 
<br />
<b>Step 10.</b> You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command under Step 7. Navigate to the evaluation folder for your trained model e.g. 
<pre> cd Tensorlfow/workspace/models/my_ssd_mobnet/eval</pre> 

<br />
