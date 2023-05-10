# Reference

---

## Papers and Strategies

1. [A Flexible Fall Detection Framework Based on Object Detection and Motion Analysis](https://ieeexplore-ieee-org.ezproxy.ugm.ac.id/stamp/stamp.jsp?tp=&arnumber=10066990)

   First detects human objects in the frame using YOLOv5, then tracks the object by using YOLOv5 every frame.

2. ~~[Improved Pedestrian Fall Detection Model Based on YOLOv5](https://ieeexplore.ieee.org/document/9930104)~~

   Doesn't use motion analysis, but uses YOLOv5 and a CNN to detect pose.

3. [Fall Detection with Pose Estimation](https://youtu.be/IlsXQPOF9IE)

4. [also pose estimation calculating hip position](https://www.mdpi.com/2073-8994/12/5/744)

## Proposed Strategy

1. Detect people in the frame
   - ~~YOLOV5~~
   - Tensorflow pose detection (movenet)
2. For each estimated pose:
   - calculate the angle of the head and the hip
     - calclulate the rotation speed
     - calculate the angular acceleration
   - calculate the position of the hip
     - calculate the difference between y velocity and acceleration
   - calculate the width and height ratio of the bounding box
3. If the angular acceleration of the head and the hip is greater than a threshold, and the difference between y velocity and acceleration is greater than a threshold, and the width > height, then the person is falling.

## Dataset

1. [Multiple cameras fall dataset](http://www.iro.umontreal.ca/~labimage/Dataset/)
