# Reference

---

## Papers

1. [A Flexible Fall Detection Framework Based on Object Detection and Motion Analysis](https://ieeexplore.ieee.org/document/10066990)

   Motion analysis

2. ~~[Improved Pedestrian Fall Detection Model Based on YOLOv5](https://ieeexplore.ieee.org/document/9930104)~~

   Doesn't use motion analysis, but uses YOLOv5 and a CNN to detect pose.

## Proposed Strategy

1. Use YOLOv5 to detect people in the frame
2. Represent each person with an ellipse bounding box / rotated bounding box. The rotation of the bounding box will determine the orientation of the person.
3. If the rotation is a certain value, then the person is considered to be falling.

## Dataset

1. [Multiple cameras fall dataset](http://www.iro.umontreal.ca/~labimage/Dataset/)
