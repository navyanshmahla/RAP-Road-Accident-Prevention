<h1><b>Using Deep Learning to prevent road accidents</b></h1>

This is my SoC project for the year 2022. The aim of project is to train and deply a sequential machine learning model that detects drowsiness, tiredness and fatigue in the eyes of car drivers. 
<br><br>
According to  National Highway Traffic Safety Administration, annually more than 1 Lakh accidents happen each year due to driver fatigue and more than 50,000 accidents happen due to drink and drive.
<br><br>
This is a major concern and needs to be resolved. 
<br>
I would like to thank my mentors <a href="https://github.com/WeRishEin">Rishi Kumar</a> and <a href="https://www.facebook.com/rishikesh.gunjal.7">Rishikesh Gunjal</a> for guiding me through this project. <br><br>

<h2><b>The Algorithm</b></h2>

<br>A basic idea that we thought to solve this problem comes from building sequential model, and using real-time camera input to detect whether the driver is fatigue or not. If the driver is fatigue, a prompt would be shown to him that he shouldn't drive.



I first trained the sequential model. The model trained with 96% of accuracy. The next step was to use OpenCV to take input from the camera and use Haar Cascade classifier to detect face, left eye and right eye.<br>
<br><img src="https://media.springernature.com/lw685/springer-static/image/chp%3A10.1007%2F978-3-030-14799-0_54/MediaObjects/480747_1_En_54_Fig5_HTML.png" width=100%> <i>A demo image showing how the model works and detects drowsiness</i><br><br><br>
 The next step was to create a rectangle as a boundary at the eyes. Store each frame in a variable and then pass those frames as jpeg format photos in the model to predict the data. If the probability of eye closed (of any one eye) is more than 0.7 for more than half of the frames in the video then the person can be termed fatigue or drowsy. In that case, the prompt is shown that the person shouldn't drive.

<br>




