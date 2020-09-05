# Mask-RCNN
Mask RCNN

Run this notebook on google colab.

Mask RCNN for Object Detection and Instance Image Segmentation.



A Brief Overview of Image Segmentation
 

Image segmentation creates a pixel-wise mask for each object in the image. This technique gives us a far more granular understanding of the object(s) in the image. The image shown below will help you to understand what image segmentation is:
 
Here, as you can see that each object (cells consider as objects) has been got segmented. This is how the image segmentation works.
There are two types of image segmentation: First Semantic Segmentation and Second Instance Segmentation. Let’s take an example to understand how both of these types of work:
 
All 5 objects present in the left image are people. Hence, semantic segmentation will classify all the people as a single instance (object). Now, the image present on the right image also has 5 objects (all are people). But here, different objects (people) of the same class have been assigned as different instances. This is a simple example of instance segmentation.
I hope that now you all understand the difference between the Semantic Segmentation and the Instance segmentation.

What is Mask R-CNN?
The Mask R-CNN algorithm was first introduced by He et al. in their paper in 2017, Mask R-CNN.
Mask R-CNN builds on the previous object detection architecture work of R-CNN (2013), Fast R-CNN (2015), and Faster R-CNN (2015), all are by Girshick et al.
The reason this method works much better is due to the robust, discriminative features learned by the CNN.

The Faster R-CNN paper by Girshick et al. is introduced Region Proposal Network (RPN) that bakes the region proposal directly into the architecture, alleviating the need for the Selective Search algorithm.
As a whole, Faster R-CNN architecture is capable of running at approx. 7-10 FPS, it is a huge step towards making real-time object detection with deep learning a reality.
Mask R-CNN algorithm builds on Faster R-CNN architecture with two major contributions:
1)	Replacing ROI Pooling module with a more accurate ROI Align module.
2)	Inserting an additional branch out of the ROI Align module.
This additional branch acquires the output of the ROI Align and then feeds it in the two CONV layers.
The output of CONV layers is the mask itself.
Now, We can further visualize the Mask R-CNN architecture in the following figure:  The Mask R-CNN work is done by He et al. replaces the ROI Polling module with an extra precise ROI Align module. The output of the ROI module is next fed into two CONV layers. The output of this CONV layers is the mask itself.

                                        A visualization of Mask R-CNN producing a 15 x 15 mask, the mask resized to the original dimensions of the image, and then finally overlapping the mask on the original image.

Step By Step Detection:
1)	Anchor Sorting and Filtering
Visualizes each step of the initial stage Region Proposal Network and illustrates positive and negative anchors along with the anchor box refinement. 
2)	Bounding Box Refinement
This is an example of terminal detection boxes (dotted lines) and the refinement applied to them (solid lines) in the next stage. 
3)	Mask Generation.
Example of generated masks. These then get scaled and then placed on the image in the right location. 
4)	Layers Activation.
Usually, it's beneficial to examine the activations at different layers to study for signs of trouble (all zeros or random noise). 
5)	Weight Histograms.
Another beneficial debugging tool is to examine weight histograms.  
6)	Logging to TensorBoard
TensorBoard is another excellent debugging and visualization API. The model is configured to log losses and save weights at the end of each epoch. 

7)	Composing the different pieces into Final Result
 


 Install the Libraries
•	NumPy
•	scipy
•	Pillow
•	cython
•	matplotlib
•	scikit-image
•	tensorflow>=1.3.0
•	keras>=2.0.8
•	OpenCV-python
•	h5py
•	imgaug
•	IPython
There is good scope in the disciplines of Geosensing, agriculture, medical image diagnostics, AR, VR, and many more. 
The deficiency of this method
1.	Adding more layers in plain nets leads to higher training errors, which result in saturation inaccuracy.
2.	Overfitting is usually faced while applying Mask RCNNs. As described in research papers, when we change camera and illumination, most RCNNs cannot perform well.   
 
 

1.	It requires a High-end GPU to get the desired results. We can't just use any processor or GPU or any laptop. This will add cost to the process.
2.	They need a large dataset to perform segmentation, which results in decreases in performance speed.


Conclusion
A blend of Semantic Segmentation and Mask-RCNN can do miracles in Object Detection and Computer Vision. The aforementioned deep learning method still can open several doors for research practitioners. Also, if you want to dive deep into the domain, you don't need to be a worry as this will live an evergreen state of the art algorithm.
