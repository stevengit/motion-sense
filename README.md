# MotionSense Dataset
This dataset includes time-series data generated by accelerometer and gyroscope sensors (attitude, gravity, userAcceleration, and rotationRate). It is collected with an iPhone 6s kept in the participant's front pocket using [SensingKit](https://www.sensingkit.org/) which collects information from [Core Motion](https://developer.apple.com/documentation/coremotion/cmdevicemotion) framework on iOS devices. A total of 24 participants in a range of gender, age, weight, and height performed 6 activities in 15 trials in the same environment and conditions: downstairs, upstairs, walking, jogging, sitting, and standing. With this dataset, we aim to look for  *personal attributes fingerprints* in time-series of sensor data, i.e. attribute-specific patterns that can be used to infer gender or personality of the data subjects in addition to their activities. 

<img src="https://github.com/mmalekzadeh/motion-sense/blob/master/materials/desc.png" class="img-responsive">
*time-series of walking activity for data subject with code 3*

## Download
  The MotionSense dataset is publicly available [in the current repository](https://github.com/mmalekzadeh/motion-sense/tree/master/data) and also [ in the Queen Mary University of London's repository]( https://goo.gl/KdZCrn) as a backup. 

## Citation
  If you use this dataset, please must cite the following paper: [TBA]

# Dataset Description
## Scenario
  For each participant, the study had been commenced by collecting their demographic (age and gender) and physically-related (height and weight) information. Then, we provided them with a dedicated smartphone (iPhone 6) and asked them to store it in their trousers' front pocket during the experiment. All the participant were asked to wear flat shoes. We then asked them to perform 6 different activities (walk downstairs, walk upstairs, sit, stand and jogging) around the Queen Mary University of London's Mile End campus. For each trial, the researcher set up the phone and gave it to the current participants, then the researcher stood in a corner. Then, the participant pressed the start button of [Crowdsense app](https://itunes.apple.com/us/app/crowdsense/id930853606?mt=8) and put it in their trousers' front pocket and performed the specified activity. We asked them to do it as natural as possible, like their everyday life. At the end of each trial, they took the phone out of their pocket and pressed the stop button. The exact places and routes for running all the activities are shown in the illustrative map in the following Figure.  

<img src="https://github.com/mmalekzadeh/motion-sense/blob/master/materials/e_map.png" class="img-responsive">

As we can see, there are 15 trials:

1. Long trials: those with number 1 to 9 with around 2 to 3 minutes duration.
2. Short trials: those with number 11 to 16 that are around 30 seconds to 1 minutes duration.

## Data Subjects
There are 24 data subjects. Here we summarized their information:

| Code | Weight (kg) | Height (cm) | Age (years) | Gender (F:0,M:1) |
| ---- | ----------- | ----------- | ----------- | ---------------- |
| 1	   | 102	       | 188	       | 46	         | 1                |
| 2	   | 72	         | 180         | 28	         | 1                |
| 3    | 48	         | 161	       | 28	         | 0                |
| 4    | 90	         | 176	       | 31	         | 1                |
| 5	   | 48	         | 164	       | 23	         | 0                |
| 6	   | 76	         | 180	       | 28	         | 1                |
| 7	   | 62	         | 175	       | 30	         | 0                | 
| 8	   | 52	         | 161	       | 24	         | 0                |
| 9	   | 93	         | 190	       | 32	         | 1                |
| 10	 | 72	         | 164	       | 31	         | 0                |
| 11	 | 70	         | 178	       | 24	         | 1                |
| 12	 | 60	         | 167	       | 33	         | 1                |
| 13	 | 60	         | 178	       | 33	         | 1                |
| 14	 | 70	         | 180	       | 35	         | 1                |
| 15	 | 70	         | 185	       | 33	         | 1                |
| 16	 | 96	         | 172	       | 29	         | 0                |
| 17	 | 76	         | 180	       | 26	         | 1                |
| 18 	 |54	         | 164	       | 26	         | 0                |
| 19	 |78	         | 164	       | 28	         | 0                |
| 20	 |88	         | 180	       | 25	         | 1                |
| 21	 |52	         | 165	       | 24	         | 1                |
| 22	 |100	         | 186	       | 31	         | 1                |
| 23	 |68	         | 170	       | 25	         | 0                |
| 24	 |74	         | 173	       | 18	         | 0                |

## Folders (and Features)
 There three different folders. Usually, you just need the **folder (A)** (DeviceMotion), because this folder includes everything that can be captured by both Accelerometer and Gyroscope. However, we also have data captured by these two sensors separately in the folder (B) and (C).  
 
### (A) DeviceMotion_data
This folder contains time-series collected by both Accelerometer and Gyroscope for all 15 trials. For every trial we have a multivariate time-seris, like this:
 
| index | attitude.roll | attitude.pitch | attitude.yaw | gravity.x | gravity.y | gravity.z | rotationRate.x | rotationRate.y | rotationRate.z | userAcceleration.x | userAcceleration.y | userAcceleration.z |
| ----- | ------------- | -------------- | ------------ | --------- | --------- | --------- | -------------- | -------------- | -------------- | ------------------ | ------------------ | ------------------ |
|0	    | -2.544349     | -1.250641	      | 2.175416	   | -0.176977 | 0.949187	| 0.260222	| -7.204869	      | 2.267762      | 0.103529       | -0.060221          |	1.576174	         | -0.091292          |
| 1	    | -2.524075	    | -1.187355	      | 2.047589	   | -0.21661	 | 0.927383	| 0.305012	| -2.554745	      | 6.548334       | -0.005139      |	0.134136           |	0.860307	        | -2.152149          |
| 2	| -2.534324	| -1.141923	| 1.990077	| -0.237286	| 0.909435	| 0.341488	| -2.38587	| 0.112576	| -0.576825	| 0.427914	| 0.442891	| -0.892025 | 
| 3	| -2.564504	| -1.098202	| 1.960054	| -0.248344	| 0.89039	| 0.381471	| -2.098059	| 0.199309	| -0.671066	 | 0.619987	| 0.007925	| -0.946626 |
| ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... |

Thus, we have time-series with 12 features:
1. attitude.roll
2. attitude.pitch
3. attitude.yaw
4. gravity.x
5. gravity.y
6. gravity.z
7. rotationRate.x
8. rotationRate.y
9. rotationRate.z
10. userAcceleration.x
11. userAcceleration.y
12. userAcceleration.z

For more information, please read this page: [CMDeviceMotion](https://developer.apple.com/documentation/coremotion/cmdevicemotion)
> The accelerometer measures the sum of two acceleration vectors: gravity and user acceleration. User acceleration is the acceleration that the user imparts to the device. Because Core Motion is able to track a device’s attitude using both the gyroscope and the accelerometer, it can differentiate between gravity and user acceleration. A CMDeviceMotion object provides both measurements in the gravity and userAcceleration properties.

 ### (B) Accelerometer_data 
 Here we just have data reported by **Accelerometer** sensor. Thus, there are just three features correspond to 3 different axes:
 1. x
 2. y
 3. z
 
 
 ### (C) Gyroscope_data
 Here we just have data reported by **Gyroscope** sensor. Thus, there are again just three features correspond to 3 different axes:
 1. x
 2. y
 3. z

## Labels
There are 6 different labels:
1. **dws**: downstairs
2. **ups**: upstairs
3. **sit**: sitting
4. **std**: standing
5. **wlk**: walking
6. **jog**: jogging
