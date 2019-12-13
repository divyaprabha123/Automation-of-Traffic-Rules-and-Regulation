# Automation of Traffic Rules and Regulation-(Solution)

The solution for the problem statement resides in solving varied sub problems as discussed below

## Detection of objects
Classes considered here are Pedestrian,Bi-cycle,Motor-cycle,Car,Truck. (auto-should be added)

custom yolo-v2,with a good fps can be used for Object detection in real time.

## Speed and direction of Vehicle

Identify detection box for each  objecy  and compute center y-coordinate of each box.

Box speed calibration is computed by mapping of box-speed in pixels/sec to vehicle-speed in km/hr (miles/Hr for some countries).
In order to Create the calibration table we will need a few clips of vehicles and their real speed and for that particular camera setup to get near to the absolute speed.

By determining the flow of detection box, the direction of the vehicle can also be identified

## Automated Number Plate Detection

It consist of  two parts: (Number Plate Detection + Number Recognition)
The Custom Yolo model can take care of the number plate Detection
data Pre Processing will help in better recognition of the number and letters.

## Helmet Detection and More that 2 people detection
This solution will help prevent two wheeler fatalities

Custom YOLO method is used. The  model only process the Frame Once and all detections can be made. It can therefore be used real time.

## Accident recognition 
This Feature can actually save that few golden minutes that lies in between life and death.
Accident dataset is available and this is treated as a classification problem using CNN.Accident recognition can call for an ambulance.

## Special Vehicle Identification
Currently due to the inability of a valid dataset other venues are pursued in search of building an ideal recognition model 

## Classifying Traffic Intensity Level
 the count of the number of Vehicle and pedestrian which can be used to estimate the traffic in real time.
This data can be used by the department to optimise the road and traffic 

## Deployment-
TensorRT(GPU) and OpenVino(CPU) Inference Engine,is to be be used to deploy the model,which will boost the system’s performance .Deepstream can be used to set the pipeline  end to end.

We have few bottlenecks with respect to the data availability and Deployment,and the Build For Digital India can act as a perfect platform for us to connect with both Technology experts as well as with the government for the problems implementation.
