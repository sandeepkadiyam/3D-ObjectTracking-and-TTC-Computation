## Report

### FP.1 Match 3D Objects
In the matchingBoundingBoxes function, I created a multi dimensional vector that keeps track of all the possible pairs of bounding boxes in the previous and current frame and the total number of their corresponding keypoint matches. Then the matching pair with the highest number of keypoint matches are inserted into the multi map.

The code for this function is implemented in the camFusion_Student.cpp from line 289-319.

### FP.2 Compute Lidar-based TTC
I used the previous task, TTC using Lidar as reference for implementing this function. To make this computation robust, I used median of lidar point's x coordinates instead of the nearest one to calculate the TTC.

The code for this function is implemented in the camFusion_Student.cpp from line 249-286.

### FP.3 Associate Keypoint Correspondences with Bounding Boxes
In the clusterKptMatchesWithROI function, the keypoint matches that belong to the bounding box are assigned to a vector. Then, the Euclidean distances of all the keypoint matches are calculated to identify the outliers. The points that are distant from the median of euclidean distances are removed.

The code for this function is implemented in the camFusion_Student.cpp from line 140-196.

### FP.4 Compute Camera-based TTC
I used the previous task, TTC using Camera as reference for implementing this function. To make this computation robust, I used median of distance ratios instead of the mean to calculate the TTC.

The code for this function is implemented in the camFusion_Student.cpp from line 200-246.

### FP.5 Performance Evaluation 1
