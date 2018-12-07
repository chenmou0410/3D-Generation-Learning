# PCL
This document is summary something about point cloud
## what is the point cloud
PCL, as an irregular data, is unordered and independent. 
## How to use convolution on point cloud
The traditional convolution in regular data(e.g, image) can effectively extract the spacial feature of 
Unlike regular data, such as image, the features of irregular data(point cloud) is coordinates and order of the points. We cannot just use a conv kernel to encode them a high level.
Thus, we need a special convolution  
### X-conv
This method comes from PointCNN
The key of PointCNN is their X-conv operator, which is a transformation matrix for weighting and permuting the input featuressimultaneously. For the input point clouds, "X-Conv is recursively applied to “project”, or “aggregate”, information from neighborhoods into fewer representative points (9 -> 5 -> 2), but each with richer information. 
From my point of view, each layer use a set of representative points to obtain the points of former layer. "The representative points fp2;ig should be the points that are beneficial for the information 'projection' or 'aggregation'”.
each point is associated
with a feature, an order index, and coordinates
