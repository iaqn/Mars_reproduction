# Mars_reproduction  
This is a reproduction of the paper **"MARS: An Instance-aware, Modular and Realistic Simulator for Autonomous Driving"**.  
The official open-source link is: [MARS GitHub Repository](https://github.com/OPEN-AIR-SUN/mars)  
Due to the large volume of data, two folders, `dataset` and `outputs`, have not been uploaded.  
However, you can view four sets of ablation experiment reports on WandB, which contain complete visualized data.  
[MARS Model - KITTI Report](https://api.wandb.ai/links/202105710102-zhejiang-university-of-technology/i19tssj9)  
[MARS Model - KITTI Report](https://api.wandb.ai/links/202105710102-zhejiang-university-of-technology/xosf9mpr)

## Quantitative Evaluation for Ablation Studies

<table>
  <tr>
    <th rowspan="2">ID</th>
    <th colspan="7">Settings</th>
    <th colspan="3">KITTI</th>
    <th colspan="3">V-KITTI</th>
  </tr>
  <tr>
    <th>Model</th>
    <th>Sampler</th>
    <th>Category</th>
    <th>$\mathcal{L}_\text{sky}$</th>
    <th>$\mathcal{L}_\text{depth}$</th>
    <th>$\mathcal{L}_\text{sem}$</th>
    <th>$\mathcal{L}_\texttt{accum}$</th>
    <th>PSNR $\uparrow$</th>
    <th>SSIM $\uparrow$</th>
    <th>LPIPS $\downarrow$</th>
    <th>PSNR $\uparrow$</th>
    <th>SSIM $\uparrow$</th>
    <th>LPIPS $\downarrow$</th>
  </tr>
  <tr style="background-color: #EFEFEF;">
    <td>1*</td>
    <td>Grid / Ours</td>
    <td>prop / c2f $\dagger$</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>25.04</strong></td>
    <td><strong>0.782</strong></td>
    <td><strong>0.175</strong></td>
    <td><strong>28.37</strong></td>
    <td><strong>0.907</strong></td>
    <td><strong>0.108</strong></td>
  </tr>
  <tr>
    <td>2</td>
    <td><strong>MLP</strong> / Ours</td>
    <td><strong>c2f</strong> / c2f</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>20.14</td>
    <td>0.589</td>
    <td>0.476</td>
    <td>22.19</td>
    <td>0.664</td>
    <td>0.409</td>
  </tr>
  <tr style="background-color: #EFEFEF;">
    <td>3</td>
    <td>Grid / Ours</td>
    <td>prop / c2f</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>&times;</td>
    <td>21.35</td>
    <td>0.713</td>
    <td>0.242</td>
    <td>27.30</td>
    <td>0.881</td>
    <td>0.130</td>
  </tr>
  <tr>
    <td>4</td>
    <td>Grid / Ours</td>
    <td>prop / c2f</td>
    <td></td>
    <td>&times;</td>
    <td></td>
    <td>&times;</td>
    <td></td>
    <td>23.68</td>
    <td>0.774</td>
    <td>0.181</td>
    <td>27.32</td>
    <td>0.881</td>
    <td>0.129</td>
  </tr>
  <tr style="background-color: #EFEFEF;">
    <td>4</td>
    <td>Grid / Ours</td>
    <td>prop / c2f</td>
    <td></td>
    <td>&times;</td>
    <td></td>
    <td>&times;</td>
    <td></td>
    <td><strong><span style="color: red;">28.27</span></strong></td>
    <td><strong><span style="color: red;">0.896</span></strong></td>
    <td><strong><span style="color: red;">0.056</span></strong></td>
    <td><strong><span style="color: blue;">27.43</span></strong></td>
    <td><strong><span style="color: blue;">0.880</span></strong></td>
    <td><strong><span style="color: blue;">0.114</span></strong></td>
  </tr>
  <tr style="background-color: #EFEFEF;">
    <td>5</td>
    <td>Grid / Ours</td>
    <td>prop / c2f</td>
    <td></td>
    <td></td>
    <td>&times;</td>
    <td></td>
    <td></td>
    <td>23.66</td>
    <td>0.769</td>
    <td>0.184</td>
    <td>27.30</td>
    <td>0.880</td>
    <td>0.128</td>
  </tr>
  <tr>
    <td>6</td>
    <td>Grid / Ours</td>
    <td>prop / c2f</td>
    <td></td>
    <td>&times;</td>
    <td></td>
    <td></td>
    <td></td>
    <td>20.07</td>
    <td>0.723</td>
    <td>0.251</td>
    <td>27.42</td>
    <td>0.863</td>
    <td>0.148</td>
  </tr>
  <tr style="background-color: #EFEFEF;">
    <td>6</td>
    <td>Grid / Ours</td>
    <td>prop / c2f</td>
    <td></td>
    <td>&times;</td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong><span style="color: red;">18.60</span></strong></td>
    <td><strong><span style="color: red;">0.589</span></strong></td>
    <td><strong><span style="color: red;">0.402</span></strong></td>
    <td><strong><span style="color: blue;">20.44</span></strong></td>
    <td><strong><span style="color: blue;">0.631</span></strong></td>
    <td><strong><span style="color: blue;">0.373</span></strong></td>
  </tr>
  <tr style="background-color: #EFEFEF;">
    <td>7</td>
    <td>Grid / <strong>MLP</strong></td>
    <td>prop / <strong>c2f</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>20.46</td>
    <td>0.709</td>
    <td>0.255</td>
    <td>26.46</td>
    <td>0.875</td>
    <td>0.132</td>
  </tr>
  <tr>
    <td>8</td>
    <td>Grid / <strong>Grid</strong></td>
    <td>prop / <strong>prop</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>22.23</td>
    <td>0.741</td>
    <td>0.211</td>
    <td>25.22</td>
    <td>0.871</td>
    <td>0.134</td>
  </tr>
  <tr style="background-color: #EFEFEF;">
    <td>9</td>
    <td>Grid / <strong>MLP</strong></td>
    <td>prop / <strong>c2f</strong></td>
    <td>&times;</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>20.98</td>
    <td>0.699</td>
    <td>0.257</td>
    <td>27.27</td>
    <td>0.881</td>
    <td>0.130</td>
  </tr>
  <tr>
    <td>10</td>
    <td>Grid / <strong>Grid</strong></td>
    <td>prop / <strong>prop</strong></td>
    <td>&times;</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>23.71</td>
    <td>0.763</td>
    <td>0.193</td>
    <td>26.65</td>
    <td>0.882</td>
    <td>0.125</td>
  </tr>
  <tr style="background-color: #EFEFEF;">
    <td>11*</td>
    <td><strong>MLP</strong> / <strong>MLP</strong></td>
    <td><strong>c2f</strong> / <strong>c2f</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>20.42</td>
    <td>0.592</td>
    <td>0.472</td>
    <td>21.77</td>
    <td>0.659</td>
    <td>0.410</td>
  </tr>
</table>

### Notes
- $\dagger$ `prop` represents proposal sampler, `c2f` represents coarse-to-fine sampler.
- * ID 1 is our default setting.
- * Red text(the second bold line) represents results from 300k iterations on the KITTI scene 06.
- * Blue text(the third bold line)  represents results from 200k iterations on the V-KITTI scene 02.<br/>
Sorry, colors cannot be displayed.

## Rendering Results
### KITTI
**Rendering result for KITTI-ID1:** 

https://github.com/user-attachments/assets/fa346d00-6df3-4491-85aa-22e8dfa852c4

**Rendering result for KITTI-ID4:** 

https://github.com/user-attachments/assets/9dc4a335-82f3-4055-8d4f-e793231c8ca6

**Rendering result for KITTI-ID6:** 

https://github.com/user-attachments/assets/3f742008-c534-4d31-9b26-4617dbeca300

### VKITTI
The reason for the video repetition is due to the binocular camera.<br/>
**Rendering result for VKITTI-ID4:**  

https://github.com/user-attachments/assets/6e4384c0-897a-4541-97e1-42877a58f03e

**Rendering result for VKITTI-ID6:**

https://github.com/user-attachments/assets/11dc77d8-fc15-49cf-aa62-53ea385054c9



## Setting Up Environment    
I use CUDA 11.8 and PyTorch 2.0.1.
### Step 1: Create and Activate Conda Environment  

First, create a new Conda environment with Python 3.9:

```bash
conda create --name mars -y python=3.9
conda activate mars
```

### Step 2: Install Required Packages   (this need  torch >= 1.13.1)
```bash
pip install mars-nerfstudio  
```
### Step 3: Clone and Build tiny-cuda-nn
```bash
git clone --recursive https://github.com/nvlabs/tiny-cuda-nn
cd tiny-cuda-nn
```
Build the project using CMake:
```bash
cmake -DCMAKE_CUDA_COMPILER=/usr/local/cuda-12.4/bin/nvcc . -B build
cmake --build build --config RelWithDebInfo -j
```
Install the PyTorch extension:
```bash
cd bindings/torch
python setup.py install
```

### References:
##### dataset download
- https://www.cvlibs.net/datasets/kitti/eval_object.php?obj_benchmark=3d
- https://www.cvlibs.net/datasets/kitti/eval_tracking.php
- https://waymo.com/open/download/
#### installation
- Pytorch Version: https://stackoverflow.com/questions/76678846/pytorch-version-for-cuda-12-2
- Cmake: https://zhuanlan.zhihu.com/p/519732843
#### resources
- https://blog.csdn.net/weixin_42896263/article/details/131978295
- https://blog.csdn.net/weixin_45818708/article/details/137588790
- https://blog.csdn.net/weixin_38842821/article/details/125933604
#### paper link
- (2th)  https://arxiv.org/abs/2111.12077
- (7th)  https://arxiv.org/abs/2107.02791
- (19th) https://arxiv.org/abs/2201.05989
- (22th) https://arxiv.org/abs/2111.14643
- (31th) https://arxiv.org/abs/2206.00665
- (34th) https://arxiv.org/abs/2103.15875

