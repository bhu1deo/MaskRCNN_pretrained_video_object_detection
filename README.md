# MaskRCNN_pretrained_video_object_detection
Used a pretrained Mask RCNN to identify, mask and label objects in a video. 
 
I do not own any part of the code. The code is inspired from Pyimagesearch blog: 
https://www.pyimagesearch.com/2018/11/19/mask-r-cnn-with-opencv/

The Mask-RCNN is an intricate model. It builds up upon 
1.) R-CNN
2.) Fast R-CNN 
3.) Faster R-CNN

The fundamental building blocks of the architecture are as follows: 

A.) The RPN : The Region proposal network:


B.) The Fast R-CNN module: 


C.) A mask generation module: 



Results on a video: 







https://user-images.githubusercontent.com/20145042/133753439-d50db098-72b4-4ef1-bb07-669a1ab640df.mov





As an aside I still don't understand what is the need for a separate mask detection layer. The bounding box regressors found by the fast R-CNN module should be used to locally enclose the object under consideration and then mask pixels should be located in that region, finally followed by inverse transforming and pasting on to the original image. 
