# Dynamic-Depth-of-Field-with-Eye-Tracking
### ECE697 - Capstone Project

College of Engineering, University of Wisconsin - Madison, WI

Neel Kelkar, Suchith Suresh, Nawal Dua

Students: ndkelkar@wisc.edu, suchithsures@wisc.edu, ndua2@wisc.edu

Professor: matthew.malloy@wisc.edu


![](example_gif.gif)


## Description

In this project, we intend to first generate depth maps from input video. Using these depth maps,
we plan to create refocusable videos.

With these refocusable videos, we can simulate human vision but with a more cinematic DoF using
eye tracking technology where the video will place more emphasis on whichever subject a viewer
looks at.

## Instructions

### Generating Depth Maps
To get the premade depth maps that work with out code, go to Google's Mannequin Challenge [repository](https://github.com/google/mannequinchallenge) and download and follow their [setup instructions](https://github.com/google/mannequinchallenge#setup). Replace the ``` run_and_save_DAVIS ``` method in ```mannequinchallenge/models/pix2pix_model.py``` by the code in [pix2pix_replacement.py](https://github.com/nawaldua/Dynamic-Depth-of-Field-with-Eye-Tracking/blob/master/code/pix2pix_replacement.py)

Comment and uncomment the parts of the replacement code as neccesary.

To get the depth maps, follow the run [instructions](https://github.com/google/mannequinchallenge#single-view-inference) on google's repo.

### Dynamic Depth of Field

Download this repository and run ```/code/main.py```


NOTES: In the GUI, choose the ‘Dynamic-Depth-of-Field-with-Eye-Tracking’ folder (project folder) as the directory as it contains the required input frames and depth maps data.
The functions in the ‘outputfuncs.py’ file are accessed/executed by clicking the following buttons from the main window:    


1. To access the Preview function and to choose the variance and blurring parameters for processing the video
Directory --> Preview --> Generate  
(Access ‘mouse_move’, ‘genpreview’, ‘preview_win’)  
OR  
2. To process a new video based on required parameters  
Directory --> View Video --> Process Video --> Output Video  
(Access ‘mouse_move’, ‘output_win’)  
OR  
3. To view a previously processed video  
3. a. (For picking the default output folder)  
Directory --> View Video --> Output Video  
3. b. (For picking a different output folder)  
Directory(Optional Step) --> View Video --> Output Folder --> Output Video  

The Process Video step will take anywhere from 30 to 200 seconds for a 480p resolution video, please check the python console for progress

List of libraries required are :
1.	tqdm
2.	time
3.	cv2 (opencv-python)
4.	numpy
5.	tkinter
6.	glob
7.	copy
8.	math

## Further Information

For a camera, Depth of Field(DoF) is the distance between the nearest and farthest object in focus.
The depth of field in a video depends on numerous factors such as focal length, aperture, distance to
subject, etc. The human eye too has a depth of field. DoF is generally extremely wide for objects
more than a few meters away, meaning that everything is in focus at the same time.
For near objects, the DoF is very shallow, giving rise to the cinematic focus effect we see in movies.
The DoF in cinematic videography is done using specialized lenses and scripted positioning of
subjects. Mobile phone videos do not have this positioning planned beforehand and thus the cameras
have a wide DoF as the default. Mobile phone camera’s don’t have readily available interchangeable
lenses either, preventing daily users to use the optimal lens for the subject.

To learn more about the project you can look at our [Project Proposal](Group1-Finalized_Project_Proposal.pdf) or our [Final Project Report](Final_Project_Report_Group_1.pdf)

## Credits

- Google's Mannequin Challenge [Dataset](https://google.github.io/mannequinchallenge/www/download.html) and [Depth Mapping Code](https://github.com/google/mannequinchallenge)

