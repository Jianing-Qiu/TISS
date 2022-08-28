# TISS

This is the data repository of our work:

**[Egocentric Human Trajectory Forecasting With a Wearable Camera and Multi-Modal Fusion](https://ieeexplore.ieee.org/document/9813561)**
<br>
Jianing Qiu, Lipeng Chen, Xiao Gu, Frank P.-W. Lo, Ya-Yen Tsai, Jiankai Sun, Jiaqi Liu, and Benny Lo
<br>
published at IEEE Robotics and Automation Letters 2022


The train and test pickle files contain the data in the following format:
```
{sample_id: {'camera_wearer_traj': the trajectory of the camera wearer (stored in the TUM trajectory format. 10 time steps in total. 
                                   The first 3 time steps are for observation, and the remaining 7 are for prediction),
             'nearby_people': the trajectories of nearby people in the observation period, and they are stored in the following format:
                              {person_index: {'center': the body center of the tracked nearby person,
                                              'bbox': the bounding box of the tracked nearby person,
                                              'keypoints': the body keypoints of the tracked nearby person},
                               ...
                              },                                                         
             'semantics_encoding': the encoding of the scene semantics in the observation period 
                                   (3 semantic segmentation maps),
             'depth_encoding': the encoding of the depth map in the observation period 
                               (3 depth maps)
            },
 ...
}
```
The pickle files contain 9992 training and 2500 test samples, respectively.
