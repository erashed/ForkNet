# ForkNet

Copyrights (c) 2019, Essam Rashed 
(essam (dot) rashed (at-sign) nitech.ac.jp), NITech, Nagoya, JP 

This code aims at mapping MRI image with segmented labels of different anatomical structures. The design of ForkNet is based on unified encoders and individual decoders. This implementation is for ForkNet (N=2) to segment MRI images of GM & WM. However, it can be easily extended to arbitrary any N.
 
This code is compatable with Mathematica 11.3 and byond and tested over Windows 10, Ubuntu 16.04, and OSX 10.11.6. More details are in our paper mentioned below. If you are using this code, please refer to our paper.

-> Input images are in MATLAB "*.mat" formats for easy use 

-> To Run Select Evaluation -> Evaluate Notebook 

-> If you are not familier with Mathematica Notebooks (*.nb), you can download free reader from here: http://www.wolfram.com/cdf-player/

-----------------------------------------------------
"ForkNet.nb"

This notebook will train the ForkNet architecture to segment MRI head image into segmented structures. The used example is just for WM and GM (for simplicity).
Input: MRI image, labels of WM, labels of GM (in *.mat) formats
Output: Trained Network + loss function (training/validation) values

-----------------------------------------------------
"UNet.nb"

This notebook will train the UNet architecture to segmnet MRI head image into WM and GM. Input and output are similar to the above notebook. Details about UNet can be found here:
https://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/

-----------------------------------------------------
"ForkNet_PreTrained.nb"

This notebook will use a pretrained network to segment MRI. Use the following papermeters for different anatomical tissue

Tissue values

1> Cerebellum

2> CSF

3> Blood

4> Bone (Cortical)

5> WM

6> Mucous tissue

7> Dura

8> Fat

9> Bone (Cancellous)

10> GM

11> Vitreous Humor

12> Muscle


-----------------------------------------------------
Other files

"Arch/ForkNet_N_2.nb" 
"Arch/UNet_N_2.nb"
"Arch/NetModules.nb"
-> Network architecture (called automatically)

"Test/ForkNet_Test.nb	" 
"Test/PreTrained_Test.nb"
"Test/UNet_Test.nb"
-> Diplay of network test (called automatically)

"Trained Networks/ForkNet_axial_G0_50_2.wlnet"
"Trained Networks/ForkNet_axial_G1_50_2.wlnet"
"Trained Networks/ForkNet_axial_G2_50_2.wlnet"
-> Trained network (called automaticallyy)

"snapshots/Training_in_progress.png"
"snapshots/SampleResults.png"
-> Snapshot images

"NAMIC/case01015.mat"
"NAMIC/case01015_WM.mat"
"NAMIC/case01015_GM.mat"
-> Sample data

-----------------------------------------------------
How to use

Open in Mathematica (11.3 or above), Evalute -> Evaluate Notebook

References
----------

* E. A. Rashed, J. Gomez-Tames, A. Hirata "Development of accurate human head model for personalized dosimetry using deep learning," NeuroImage, 116132, 2019 (doi: https://doi.org/10.1016/j.neuroimage.2019.116132)

* E. A. Rashed, J. Gomez-Tames and A. Hirata, "Generation of head models for brain stimulation using deep convolution networks," IEEE International Conference on Image Processing (ICIP2019), Taipei, Taiwan, Sept. 2019 (doi: https://doi.org/10.1109/ICIP.2019.8803334)
