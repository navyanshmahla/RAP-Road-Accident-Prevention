<h1>Where to get the dataset from?</h1>

<br>
I found a an exhaustive collection of data set for closed and opened grayscale images for each eye on Kaggle. The link to the data set: 
<br>
<a href="https://www.kaggle.com/datasets/prasadvpatil/eye-dataset"> Kaggle Eye Opened and Closed Dataset</a>
<br>
I used this dataset to train my model using Keras. 
Although I manipulated the dataset to ease the workflow of my project. Like:
<ul>
<li>I changed the file name corresponding to the close or open eye. Eg: For open right eye, the files were named open-right(1).jpg, open-right(2).jpg, and so on. </li>
<li>I made the folder for training, validation and testing of the dataset. And randomly moved the files for each opened and closed eye folder. For example: There were total of three folders inside the root directory of the dataset repository. Those three folders are train, valid and test. Inside each of these folders, there are two sub-folders named open and close. Open containing opened eyes images and close containing closes eye images. </li>
<li>I assigned total of 1000 images for train folder, 200 for valid folder and 100 for test folder.</li>
</ul>
In this way I manipulated the data to train the model in a much more organised way. The data folder can be found on my drive <a href="https://drive.google.com/drive/folders/1xlmIVKkZP3aPThEsvP0AUBNelTTlCnk1?usp=sharing">here </a>. 