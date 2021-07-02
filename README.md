# Cone-beam-CT-scatter-correction-tool
Cone beam CT scatter correction tool via the multiple spectral model

Introduction
Cone beam CT scatter correction tool is a software that can correct the scatter artifacts in the CBCT images. The software applies the trained multiple spectral scatter estimation model which is proposed in the paper ‘A generalized image quality improvement strategy of cone-beam CT using multiple spectral CT labels in Pix2pix GAN’. The software has the functions of scatter correction and CT reconstruction. The input is the uncorrected CBCT projection image, and the outputs are the corrected projection image and the corrected CBCT image.
![image](https://user-images.githubusercontent.com/86813489/124226681-14e4ed00-db3c-11eb-9ebf-ab49bdeb8508.png)

Setting
The interface of the software includes the basic setting, path setting, image display and result showing. 
Basic setting
Task: choose the scatter estimation model.
Mode: choose the scanning mode (halffan or fullfan) and determine the path of reconstruction program.
Width: the width of the projection.
Height: the height of the projection. (Tips: the width and the height should be multiples of 256).
Ratio: control the intensity of the estimated scatter signal. The value of the ratio is close to 1. 
Path setting
Input path: the path of the uncorrected projection. 
Save path: the path to save the corrected projection.
Recon path: the path of the input file for reconstruction. The ‘fdk.in’ in the package is an example of the recon path.
Display: show the uncorrected projection after the input path selected and the corrected projection or the corrected CBCT image after processing.
Result: show the task, device and calculation time of the software.


Quick Start
After starting the software and entering the basic setting, there are two options:
1.	To process a single projection, click ‘Load Image’, select the projection path, and then select the save path. Finally, click ‘Infer Model’ to start processing. 
This process will not start the reconstruction process.
2.	To process the complete projection data, click ‘Open Folder’, select the path of the folder where the projection is located, and then select the save path and the recon path. 
Finally, click ‘Infer Model’ to start processing. After the processing is completed, the reconstruction program will be started for reconstruction.

References
Yangkang Jiang, Chen Luo, Pengfei Yang, Jing Wang, Wei Zhao and Tianye Niu*, " A generalized image quality improvement strategy of cone-beam CT using multiple spectral CT labels in Pix2pix GAN." 

Requirement
Scatter correction: can be run on CPU and GPU. If using GPU, CUDA and CUDNN are required to be installed.
Scatter correction and reconstruction: can only be run on GPU. CUDA and CUDNN are required to be installed.

Contact
If you have any questions or suggestions about this software, please contact us:
Dr. Tianye Niu: tyniu@gatech.edu
Mr. Yangkang Jiang 11718077@zju.edu.cn



