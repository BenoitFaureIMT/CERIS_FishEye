# CERIS_FishEye

This repository contains the dataset developed by students at the CERIS Labatory of IMT Mines Ales. Each branch contains a different part of the dataset. The descriptions of each parts of the dataset are as followed:

Dataset_Section_1 : train - 1492 images | valid - 377 images
- Images pulled from videos taken inside the workshop of the CERIS Labatory, this images are dark. The camera is still. 0-3 people can be seen.
- Images pulled from videos taken right outside the workshop of the CERIS Labatory during a sunny day, this images are bright. The camera is still. 0-2 people can be seen.
Images were taken every 6th frame.

Dataset_Section_2 : train - 390 images | valid - 101 images
- Images pulled from videos taken with the camera in motion while :
    - Walking around the campus
    - Walking along the street outside the campus
Images were taken every 10th frame. 0-30 people can be seen.

Mirror_Word : train - 821 images | valid - 204 images
- Images pulled from the Mirror Word dataset and reannotated.

Data is stored in the YOLOv5 training format. Details are as followed :

parent directory :
- data.yaml -> relative path of train and valid directorys , number of annotations and name of annotations as a list
- train direcory
- valid directory

train/valid directory :
- images -> contains all images
- labels -> contains labels, name of the file equals the name of the image the label corresponds to

labels.txt -> each line corresponds to a different object being labeled, each caracteristic is separated by a space (in the following description I will use a |)

    index of the label in the list of names defined in data.yaml | coordinate x | coordinate y | width | height of the label
    
All coordinates and dimensions are normalized, this means to get the actual dimension in pixel, multiply by the actual width/height of the image
