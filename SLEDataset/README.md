# Benchmark dataset for performance evaluation of inertial sensor-based step length estimation models.

## Summary

Benchmark dataset for performance evaluation of inertial sensor-based step length estimation models. It contains more than 22 km of gait measurements in JSON format for 15 healthy adults for three walking speeds, four sensor positions typical of smartphone users, and two independent sets of field tests: one for tuning the models' constants and the other one for the performance evaluation of the models. Altogether, 360 tests were conducted.

## Description of experiment

Raw linear acceleration and orientation sensor measurements were obtained from a group of 15 healthy adults (10 men and five women). Considering smartphone's local coordinate system, the following positions were tested:

1.	**Pocket.** Smartphone is carried in the front right trousers’ pocket. Z-axis is pointing in the walking direction and y-axis is pointing in the opposite direction of the floor. Smartphone’s position is fixed. 
2.	**Bag.** Smartphone is carried in the pocket inside the bag. Its x-axis is pointing in the walking direction and its screen is turned away from the user's body so that the z-axis is parallel to floor. Smartphone's position is fixed and the bag is handheld.
3.	**Hand-reading.** Smartphone is held by the user in the right hand in front of him/her so that the screen is parallel to floor and pointing in the opposite direction of the floor. Smartphone's y-axis is pointing in the walking direction and its position is fixed.
4.	**Hand-swinging.** The user is holding the smartphone in the right hand, which is lowered. Smartphone's y-axis is pointing in the walking direction and its screen is turned towards the user's body so that the z-axis is parallel to floor. Smartphone's position is fixed.

Sensor data were acquired using Samsung Galaxy S7 edge smartphone. They were sampled at 100 Hz with standard deviation of 8 Hz together with timestamps. Next, sensor data were resampled to 100 Hz using linear interpolation. 

Two independent sets of field tests were conducted for two straight test paths: 15- and 108-m-long. Every person walked each path carrying the smartphone as in the previously described four scenarios at three different steady walking speeds: slow, normal and fast. People self-selected walking speeds to their preference, but were asked to maintain the walking speed as similar as possible during all tests for the same speed.



## Dataset description

This dataset contains 15 folders (person1, person2, …, person15) that include measurements for each person: subfolder test_path1 for the shorter and subfolder test_path2 for the longer test path. Every file stores data collected in one test formatted in a JSON object that contains the following keys:
-	**smartphone_position** denotes the position of smartphone during the test. Possible values are specified in string data type and limited to pocket, hand-reading, hand-swinging and bag. 
-	**walking_speed** denotes the walking speed of the person during the test. Possible values are slow, normal and fast.  
-	**path_length** denotes the length of test path. The value is specified in meters.
-	**height** denotes the height of person. The value is specified in meters.
-	**leg_length** denotes the length of the person’s leg. The value is specified in meters.
-	**gender** denotes person’s gender. Possible values are specified in string data type and limited to male and female.
-	**sampling_frequency** denotes the sampling frequency in hertz. The value is 100.
-	**linear_acceleration** denotes linear acceleration. The value is a JSON object that contains the following keys that label triaxial linear acceleration data:
	*	**x** denotes x-axis of smartphone’s local coordinate system. The value is an array of numbers containing x-axis data. 
	*	**y** denotes y-axis of smartphone’s local coordinate system. The value is an array of numbers containing y-axis data. 
	*	**z** denotes z-axis of smartphone’s local coordinate system. The value is an array of numbers containing z-axis data. 
-	**orientation** denotes the orientation of the smartphone. The value is a JSON object that contains the following keys that label triaxial orientation sensor data:
	*	**x** denotes x-axis of smartphone’s local coordinate system. The value is an array of numbers containing x-axis data. 
	*	**y** denotes y-axis of smartphone’s local coordinate system. The value is an array of numbers containing y-axis data. 
	*	**z** denotes z-axis of smartphone’s local coordinate system. The value is an array of numbers containing z-axis data. 



