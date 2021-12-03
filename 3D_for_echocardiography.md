#                    3D for echocardiography



## Problem Statement

- We are supposed to make a 3D model of heart using the 2D images given in different planes.
- An echo image of the heart is available on three different planes, as defined below –
  Three SAX images (basal, mid-cavity and apical) in the X-Y plane
  A4C in the X-Z plane
  A2C in the Y-Z plane
- Their contours are given in all the images and they are like projections of an object in the front, top and side view.
- The problem is to combine the 5 contours in the five images (3 SAX and 2 LAX) to create a 3D model of the heart, as shown on RHS.

## Our Approach

- A dicom is a echocardiography of the heart given to us as a dataset
- We analyzed the dataset consisting of dicom images and plotted contours for it using the co-ordinates
- We did linear 3D transformations: Translation, Rotation, Shearing, Reflection to get homogeneous co- ordinates in 3d dimension.
- Using the fastai library, we recognized the total number of frames each dicom image has and analyzed the frames with matplot library. 
- We used matplot library to plot 2d co ordinates from the dataset
- From the same library, we tried to convert 2d to 3d and analyzed 
- We used numpy library for matrix transformation and transformed every view towards a threshold 3D point

## Files Description

- Anotatefirstframe - This file is used to draw contours and to read dicom images using the library pydicom and save the contour co ordinates as a real number in _inx.txt file.
- dicom.ipynb- We used fastai library to find the frames from a dicom and analyze the heart diastole and systole from each frame present in the dicom. 
- Hifive.ipynb- This file is used to plot the 3 homogenous x,y,z co-ordinates which we got after matrix transformation and plot the 3D heart projection. 

