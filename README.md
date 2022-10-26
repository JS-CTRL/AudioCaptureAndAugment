# Get and Augment Audio 
## Purpose:
This is an all in one program allows you to:
* Record audio samples 1 second long at a sampling rate of 16kHz
* Augment those samples using:
	* Noise injection
	* Time shifting
	* Pitch shifting 
* All audio augments check current sample count and print out final sample count based on user parameters allowing the user to customize both the level of impact that the augment will have as well as how many files in total will be created
* Augmentations are documented in file name for example:
	*  *sample_Pitch_Shift_**X**_**Y***- indicates that this sample is sample **Y** and has been through the shift loop **X** times
	* *sample**X**_Noise**Y**_Multiplier**Z***- indicates that this is sample **X** , has been augmented using noise **Y** at a amplitude multiplier of **Z**

### Record Samples
Record, visualize and listen to audio samples
![Audio Capture](https://github.com/JS-CTRL/AudioCaptureAndAugment/blob/main/Images/audioCapture.PNG?raw=true =400x300)
### Augment: Noise
Add custom captured noise overlay to audio samples at increasing amplitudes
![NoiseOverlay](https://github.com/JS-CTRL/AudioCaptureAndAugment/blob/main/Images/noiseOverlay.PNG?raw=true )
Listen to augmented audio
![NoiseOverlayListen](https://github.com/JS-CTRL/AudioCaptureAndAugment/blob/main/Images/noiseOverlayListen.PNG?raw=true =175x250)
### Augment: Time Shift
Shift audio forward or backward in 1/8s increments
![TimeShiftVisual](https://github.com/JS-CTRL/AudioCaptureAndAugment/blob/main/Images/timeShift.PNG?raw=true)
Listen to augmented audio
![TimeShiftListen](https://github.com/JS-CTRL/AudioCaptureAndAugment/blob/main/Images/timeShiftListen.PNG?raw=true =200x400)

### Augment: Pitch Shift
Pitch shift allows the user to input the desired final sample count and will continue to create increasingly pitch shifted samples until the desired final sample count is achieved. 

This looping function is accomplished by using the doubling equation below in order to determine the minimum required loop count.
![DoublingEquation](https://github.com/JS-CTRL/AudioCaptureAndAugment/blob/main/Images/doublingEquation.PNG?raw=true)

Each time the loop count itterates the total audio samples doubles except for the last ittration where the loop will break once final sample count is achieved. Below is a visualization of the doubling with the files created in that loop count having a new color (assuming there was 1 initial sample). Loop 5 shows 16 new samples created in that loop, 8 new samples in loop 4, 4 new samples in loop 3 etc..  
![LoopVisualization](https://github.com/JS-CTRL/AudioCaptureAndAugment/blob/main/Images/loopVisualizaton.PNG?raw=true =500x550)
Below is the pitch shifted audio visualization, notice that although the image appears similar across all pitch shift the sample amplitudes are changing.
![PitchShiftVisual](https://github.com/JS-CTRL/AudioCaptureAndAugment/blob/main/Images/pitchShiftVisual.PNG?raw=true)

Listen to augmented audio 


![PitchShiftListen](https://github.com/JS-CTRL/AudioCaptureAndAugment/blob/main/Images/pitchShiftListen.PNG?raw=true =175x400)

As part of the project that this code was written for a text document consisting of samples to use for a ML validation test needed to be created. By setting the desired number of samples to add to this document a randomized list of samples will be added accordingly. 






![Validation](https://github.com/JS-CTRL/AudioCaptureAndAugment/blob/main/Images/validation.PNG?raw=true =400x300)
