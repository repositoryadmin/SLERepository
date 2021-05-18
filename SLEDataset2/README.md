# Benchmark dataset for performance evaluation of inertial sensor-based step length estimation models.

## Summary

Benchmark dataset for performance evaluation of inertial sensor-based step length estimation models. It contains more than 10 h of gait measurements in JSON format for 10 healthy adults for long-term walking. Four walking speeds and four smartphone positions were tested on a treadmill and test polygon, each trial lasted approximately 15 min.

## Description of experiment

For detailed description of the experiment please refer to the article: ________________________

Linear acceleration sensor measurements were obtained from a group of 10 healthy adults (six men and four women). Considering the smartphone's local coordinate system, the following positions were tested:

1.	**Upper arm.** Smartphone is attached to the upper arm. The x-axis is pointing in the walking direction and the y-axis is pointing in the opposite direction of the floor. Smartphone’s position is fixed. 
2.	**Hand.** Smartphone is attached to the hand. Its y-axis is pointing in the walking direction and its x-axis is pointing in the direction of the floor. Smartphone’s position is fixed. 
3.	**Pelvis.** Smartphone is attached to the pelvis. Its y-axis is pointing in the walking direction and its x-axis is pointing in the direction of the floor. Smartphone’s position is fixed.
4.	**Thigh.** Smartphone is attached to the thigh. The x-axis is pointing in the walking direction and the y-axis is pointing in the opposite direction of the floor. Smartphone’s position is fixed. 

Sensor data were acquired using four off-the-shelf smartphones. Two sets of field tests were conducted: one on the treadmill and the other one on the rectangular-shaped test polygon.

During the treadmill experiments, slow, normal, and fast walking speeds were tested, whereas on the rectangular-shaped test polygon, the participants' self-selected preferred walking speed was tested. Every person carried all smartphones as in the previously described scenarios testing the described walking speeds. Participants self-selected the preferred walking speeds to their preference but they were asked to maintain the walking speed as similar as possible during the trial.

## Dataset description

This dataset contains 10 folders (person01, person02, …, person10) that include measurements acquired for each person in the subfolders that denote the walking speed. Every file stores data collected in one trial for the selected walking speed (either on the treadmill or on the test polygon) formatted in a JSON object that contains the following keys:
-	**smartphone_position** denotes the position of the smartphone during the test. Possible values are specified in string data type and limited to the upper arm, hand, pelvis, and thigh. 
-	**walking_speed** denotes the walking speed of the person during the test. Possible values are slow, normal, fast, and preferred. The first three walking speeds were tested on the treadmill, whereas the preferred walking speed was tested on the rectangular-shaped test polygon.  
-	**path_length** denotes the length of the test path. The value is specified in meters. This field is only present if the walking speed is preferred.
- 	**stride_lengths** denotes the stride lengths. Their values are specified in meters. This field is only present if the walking speed is slow, normal, or fast (treadmill experiments).
-	**height** denotes the height of the person. The value is specified in meters.
-	**leg_length** denotes the length of the person’s leg. The value is specified in meters.
-	**gender** denotes the person’s gender. Possible values are specified in string data type and limited to male and female.
-	**sampling_frequency** denotes the data frequency in hertz. The value is 100.
-	**linear_acceleration** denotes the triaxial linear acceleration. The value is a JSON object that contains the following keys that label triaxial linear acceleration data:
	*	**x** denotes the x-axis of the smartphone’s local coordinate system. The value is an array of numbers containing x-axis data. 
	*	**y** denotes the y-axis of the smartphone’s local coordinate system. The value is an array of numbers containing y-axis data. 
	*	**z** denotes the z-axis of the smartphone’s local coordinate system. The value is an array of numbers containing z-axis data. 
	
## Contact

Principal researcher: Melanija Vezočnik* </br>
Collaborator: Prof. Dr. Roman Kamnik** </br>
Supervisor: Prof. Dr. Matjaz B. Juric*

E-mail: contact.sle.repository@gmail.com

\* Laboratory for Integration of Information Systems </br>
   University of Ljubljana </br> 
   Faculty of Computer and Information Science </br> 
   Slovenia

** Laboratory of Robotics </br>
   University of Ljubljana </br> 
   Faculty of Electrical Engineering </br> 
   Slovenia




