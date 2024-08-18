# WideIRSTD Dataset for ICPR 2024 Resource-Limited Infrared Small Target Detection Challenge

This is the official website of the **WideIRSTD** dataset.

## 1. Dataset Description

<p align="center"> <img src="figs/dataset.png" width="70%"> </p>
<p align="center">Fig. 1. An illustration of WideIRSTD dataset.</p>

WideIRSTD dataset consists of seven public datasets: SIRST-V2, IRSTD-1K, IRDST, NUDT-SIRST, NUDT-SIRST-Sea, NUDT-MIRSDT, Anti-UAV, and a dataset developed by the team of National University of Defense Technology (NUDT), including simulated land-based and space-based data, and real manually annotated space-based data. As shown in Fig. 1, the dataset contains images with various target shapes (e.g., point target, spotted target, extended target), wavelengths (e.g., near-infrared, shortwave infrared and thermal), image resolution (e.g., 256, 512, 1024, 3200, etc.), at varied imaging systems (e.g., land-based, aerial-based and space-based imaging systems). Figure 2 shows some example images of the training sets.

<p align="center"> <img src="figs/example_data.png" width="70%"> </p>
<p align="center">Fig. 2. Example images of WideIRSTD dataset.</p>

In LimitIRSTD challenge, this dataset is used to evaluate the performance of infrared small target detection (IRSTD) under resource-limited conditions (e.g., Track 1: Weakly Supervised IRSTD Under Single Point Supervision, Track 2: Lightweight IRSTD Pixel-level Supervision). 

For track 1, "WideIRSTD-Full" dataset contains 6000 images with coarse point annotation (i.e., GT point is located around the centroid of the GT mask under Gaussian distribution) or training, and 500 images are used for test.

For track 2, "WideIRSTD-Weak" dataset contains 9000 images with groundtruth (GT) mask annotation for training, and 2000 images are used for test.


## 2. Downloads

Download for track 1 "WideIRSTD-Weak" dataset. [[BaiduYun](https://pan.baidu.com/s/1x7mtLMtxpC8Oxm4sa9Y9mA?pwd=1113)]

Download for track 2 "WideIRSTD-Full" dataset. [[BaiduYun](https://pan.baidu.com/s/1qAO67_h46CWCoTyd3sot2Q?pwd=1113)]

## 3. Challenge Results

Results of Track 1:
|Rank|	Team Name|	Score|	IoU (1e-2)|	Pd (1e-2)|	Fa (1e-6)|
|:--------:| :---------:|:--------:|:--------:| :---------:|:--------:|
|1|	Chainey|	60.7869|	45.3729|	76.2010|	24.8629|
|2|	XJTU-IR	|60.3803|	42.564|	78.1966|	26.5012|
|3|	MCV-TEAM|	60.0276|	38.9762|	81.0790|	24.6809|
|4|	Stars Twinkle and Shine|	55.2378|	42.4787|	67.997|	12.4483|
|5|	MIG| 	54.1322|	35.9067|	72.3577|	38.687|
|6|	ISTDGroup_XDH|	53.8369|	39.8986|	67.7753|	10.1781|
|7|	Banyan City|	53.6450|	34.5628|	72.7272|	15.5559|
|8|	GrapeJasmine|	52.5642|	38.8313|	66.2971|	6.5323|
|9|	EDL|	52.4566|	35.2163|	69.6969|	31.0286|
|10|	NJUST-MILab|	50.7498|	34.4634|	67.0362|	14.5339|
|11|	Hot search squad|	48.5406|	21.6193|	75.6419|	75.7045|

Results of Track 2:
|Rank|	Team Name|	Score|	mIoU (1e-2)|	Pd (1e-2)|	Fa (1e-6)|	Params(M)|	GFLOPs|
|:--------:| :---------:|:--------:|:--------:| :---------:|:--------:|:--------:| :---------:|
|1|	Chainey|	77.6729|	33.8738|	78.4534|	60.9312|	0.0288|	0.0426|
|2|	Stars Twinkle and Shine|	77.0699|	38.2523|	75.3753|	32.755|	0.0469|	0.4065|
|3|	MCV-TEAM|	76.2318|	30.5698|	77.2710|	46.4470|	0.0199|	0.2530|
|4|	BIT_CQRS|	75.8502|	36.4748|	70.7957|	30.9488|	0.0262|	0.3379|
|5|	311-IRSTD|	75.3376|	36.5870|	69.3506|	32.6290|	0.0357|	0.3742|
|6|	Lightweight infrared intelligent detection|	74.9502|	33.1144|	69.7635|	48.4658|	0.0075|	0.3438|
|7|	4L&1H|	74.6304|	34.3826|	69.5758|	40.9610|	0.0399|	0.4574|
|8|	cqu-team|	74.4930|	33.8961|	67.0983|	42.1918|	0.0230|	0.2493|
|9|	MIG|	74.3454|	31.3492|	69.3130|	64.5594|	0.0200|	0.2989|
|10|	NpuBugFree|	73.5449|	31.3861|	67.4924|	60.1341|	0.0445|	0.3388|
|11|	代码敲得队|	73.3859|	31.6169|	69.1816|	50.1419|	0.0671|	0.5322|

        
## 4. Contact
Please contact yingxinyi18@nudt.edu.cn if you have any questions.

## 5. Baseline Methods
1. Track 1: Mapping Degeneration Meets Label Evolution: Learning Infrared Small Target Detection with Single Point Supervision 

    Code: [[Github]](https://github.com/XinyiYing/LESPS) 
    
    Checkpoints: [[BaiduYun]](https://pan.baidu.com/s/1OkquXuwLztXJhto6cTRjtg?pwd=1113) [[Onedrive]](https://1drv.ms/u/s!AoFCxCGMfhW6qhrLIoDFdSCZhz7q?e=Q6cWM5)

    Results:

    |Method|	Score|	IoU (1e-2)|	Pd (1e-2)|	Fa (1e-6)|
    |:--------:| :---------:|:--------:|:--------:| :---------:|
    |DNANet_full (full supervision)|54.681|40.773|68.588|4.915e-6|
    |DNANet_LESPS_coarse (weak supervision)	|46.451|29.266|	63.636|	2.294e-5|
2. Track 2: Weighted Res-UNet for High-Quality Retina Vessel Segmentation

    Code: [[Github]](https://github.com/YeRen123455/ICPR-Track2-LightWeight) 
    
    Checkpoints: [[BaiduYun]](https://pan.baidu.com/s/1RxdttZnZBhuPqQOCqUbbBw?pwd=hge6) [[Onedrive]](https://1drv.ms/u/c/90bf30fdc8dd9ee7/EVxOhbh2Z5hOmhuejKJRM80BJ4HYRSDUSCh0YQkwWt-R-w?e=FXL6ro)
    
    Results:
        
    |Method|Score|	mIoU (1e-2)|	Pd (1e-2)|	Fa (1e-6)|	Params(M)|	GFLOPs|
    |:--------:| :---------:|:--------:|:--------:| :---------:|:--------:|:--------:|
    |UNet|51.954|34.573|55.556|18.838e-6|5.179|0.914|
