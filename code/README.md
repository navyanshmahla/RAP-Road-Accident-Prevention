<h1>Training the model</h1>

I have used Keras API for training the model. Sequential model was used for this purpose alongwith relu activation function for the first two layers and softmax activation function for the final output layer.<br>
<br>
Adam optimiser is used with a learning rate of 0.001. Categotical Crossentropy loss function was used to minimise the loss and optimise the model well. 

<br>
Model gave 98.50% accuracy with the training data. The accuracy can be improved by various methods one of which is organising the folders well into left and right eyes as well in order for the algorithm to judge which eye is closed and which one is open. But however, that would be an overkill as 98.50% accuracy is more than enough and would fulfill our requirments. 
<br>
The code was written and run on <a href="https://colab.research.google.com/drive/1lRH-1Aeo0-L_2MF6kkqrDfbGJihSCSuq#scrollTo=fSSXwG-9tEt_">Google Colab</a>.
<br><br><br>
<h1>Applying the model realtime on input taken from webcam</h1>

<br>
I used the model to predict the drowsiness of the person. For that OpenCV was used in order to predict the results. You can see them in <a href="https://github.com/navyanshmahla/RAP-Road-Accident-Prevention/blob/main/code/main.py"> main.py </a> file. Video was taken from the webcam realtime and each frame was stored in the frame variable. Frames were then passed through the haar cascade classifier which detected the face and the eyes. The eyes were distinguished with an encircled rectangular boundary. The snapshots of the eyes were taken and passed thorugh the CNN.<br>  Now there are some if else statements added. If the probability of eye opened is more than 0.85, then the eye is considered fully opened. And if the probability is less than that of 0.20 then it is considered close. If there are cases when the driver needs to be alerted then sound is played (used from PyGame framework's sound library) to alert the driver about it. 

<br>

That in short was the short explanation of the working of the model and its implementation on the data acquired from the webcam. 