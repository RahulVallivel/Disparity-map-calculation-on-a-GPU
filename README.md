# Disparity-map-calculation-on-a-GPU
Run the main.py  file the output disparity map will be stored in data folder. 
The data folder contains the input images, im0 is left image and im6 is right image, disp6 is the group truth disparity map.

host_code.py which contains the kernel code which runs on the GPU and disparity.py runs on The CPU. By default main.py will call the GPU code. 
The disparity calculation and sub-pixel estimation are implemented in the kernel.

Each image takes about 28.275ms in GPU and 128 s in CPU. Which translates to about 38 FPS in GPU and 0.5 FPS in CPU.

The error between the Ground truth and the output disparity can be calculated by running error.py.


### Results

##### Disparity map before filtering
<img src="https://github.com/RahulVallivel/Disparity-map-calculation-on-a-GPU/blob/master/img/GPU_raw.png" width="248">

##### Disparity map after filtering
<img src="https://github.com/RahulVallivel/Disparity-map-calculation-on-a-GPU/blob/master/img/GPU_Filtered.png" width="248">
