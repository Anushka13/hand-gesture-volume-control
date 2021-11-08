# hand-gesture-volume-control
This is a simple program to control volume of your system with a simple hand gesture. 
I have used opencv, mediapipe and pycaw in this project. 
Live video through webcam is processed on ssytem with opencv and mediapipe is responsible for detecting hands and various landmarks. With pyacw I was able to get the mi nand max volume range for my system and also set the volume according to my hand gesture.
This program first detects  the thumb and index fingers, finds distance between them. I have found the maximum and minimum possible distance between the fingers and converted them into the available system volume range with help of np.interp() function. Then as the length between index and thumb finger's tips change, this length is converted in accordance to available system volume range and sys. volume is then set by function setMasterVolumeLevel()
