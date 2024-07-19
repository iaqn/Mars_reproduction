# Mars_reproduction
这是对论文《MARS: An Instance-aware, Modular and Realistic Simulator for Autonomous Driving》的复现。  
官方开源链接为：[MARS GitHub 仓库](https://github.com/OPEN-AIR-SUN/mars)
由于数据量过于庞大的原因，有两个文件夹`dataset`和`outputs`并没有上传。
不过在这里，你可以查看四组消融实验的wanb报告，里面有完整可视化的数据。
[MARS模型-KITTI报告](https://api.wandb.ai/links/202105710102-zhejiang-university-of-technology/i19tssj9)
[MARS模型-KITTI报告](https://api.wandb.ai/links/202105710102-zhejiang-university-of-technology/xosf9mpr)

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

## 渲染结果
### KITTI
**KITTI-ID1 的渲染结果:**

https://github.com/user-attachments/assets/fa346d00-6df3-4491-85aa-22e8dfa852c4

**KITTI-ID4 的渲染结果:**

https://github.com/user-attachments/assets/9dc4a335-82f3-4055-8d4f-e793231c8ca6

**KITTI-ID6 的渲染结果:**

https://github.com/user-attachments/assets/3f742008-c534-4d31-9b26-4617dbeca300

### VKITTI
**VKITTI-ID4 的渲染结果:**

https://github.com/user-attachments/assets/6e4384c0-897a-4541-97e1-42877a58f03e

**VKITTI-ID6 的渲染结果:**

https://github.com/user-attachments/assets/11dc77d8-fc15-49cf-aa62-53ea385054c9

