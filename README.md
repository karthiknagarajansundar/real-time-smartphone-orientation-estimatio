# Real time smartphone orientation estimation

## Objective
The goal of this project is to develop and implement an Extended Kalman filter (EKF) that performs orientation estimation, in real time, based on measurements provided by (streamed from) a standard smartphone.

## Experiments
### Angle estimations: EKF without any measurment updates
<img src="https://github.com/karthiknagarajansundar/real-time-smartphone-orientation-estimation/blob/main/Images/task5_timeUpdate_eul.png" width="310" height="310"> <img src="https://github.com/karthiknagarajansundar/real-time-smartphone-orientation-estimation/blob/main/Images/task5_tilted_start_eul.png" width="310" height="310"> <img src="https://github.com/karthiknagarajansundar/real-time-smartphone-orientation-estimation/blob/main/Images/task5_shake_eul.png" width="310" height="310">
#### Estimates when rotated 90° about x,y,z  | Estimates when tilted in one direction | Estimates when shaking the phone along the surface

### Angle estimations: EKF with accelerometer update
<img src="https://github.com/karthiknagarajansundar/real-time-smartphone-orientation-estimation/blob/main/Images/task7_timeUpdate_eul.png" width="320" height="320"> <img src="https://github.com/karthiknagarajansundar/real-time-smartphone-orientation-estimation/blob/main/Images/task7_shake_eul.png" width="320" height="320"> <img src="https://github.com/karthiknagarajansundar/real-time-smartphone-orientation-estimation/blob/main/Images/task8_outlier_rej_eul.png" width="320" height="320">
#### Estimates with accelerometer update  | Estimates while the phone was made to slide | Estimates with outlier rejection  

### Angle estimations: EKF with magnetometer update
<img src="https://github.com/karthiknagarajansundar/real-time-smartphone-orientation-estimation/blob/main/Images/task10_facing_eul.png" width="320" height="320"> <img src="https://github.com/karthiknagarajansundar/real-time-smartphone-orientation-estimation/blob/main/Images/task10_mag_dist_eul.png" width="320" height="320"> <img src="https://github.com/karthiknagarajansundar/real-time-smartphone-orientation-estimation/blob/main/Images/task11_outlier_rej_eul.png" width="320" height="320">
#### Estimates with magnetometer update | Estimates when exposed to magnetic disturbance | Estimates with outlier rejection 

### Experimentation with different combinations of sensors
<img src="https://github.com/karthiknagarajansundar/real-time-smartphone-orientation-estimation/blob/main/Images/task12_acc_mag.png" width="450" height="450"> <img src="https://github.com/karthiknagarajansundar/real-time-smartphone-orientation-estimation/blob/main/Images/task12_gyr_mag2.png" width="450" height="450">
#### Using only accelerometer and the magnetometer | Using  the  gyroscope  and  magnetometer

## Conclusion
Through the experiments, each sensor contributes to the estimation of the orientation in different ways. The gyroscope allowed the estimates to track the fast dynamics
in rotations. On the other hand, accelerometer allowed to measure the absolute orientation of the phone while, the magnetometer ensured the bearing of the sensors to be known.
Different combinations allowed for varied performances but estimation was observed to be best when all three sensor data are included.

## License
[MIT License](https://github.com/karthiknagarajansundar/real-time-smartphone-orientation-estimation/blob/main/LICENSE)
