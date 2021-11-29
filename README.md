# GAN-based Synthetic Medical Image Augmentation for increased CNN Performance
## 2021 Hallym University Capstone Design

Team Members:
이승리, 서영재, 서원진, 최재홍

-----

## Project Overview


 먼저 일반 데이터와 기본적인 augmentation을 적용하여 학습을 진행한다. 모델은 U-Net구조를 참고하여 구축하고 성능을 확인한다. Pix2Pix를 통해 생성된 fake image를 train dataset에 추가한다. 그 후 새로 구성한 데이터셋으로 Segmentation 작업을 수행하는데 정확한 비교를 위해 하이퍼 파라미터의 값은 고정하여 학습을 진행한다.

## Dataset

데이터셋은 캐글 대회에서 제공한 데이터입니다. 

[**MOAI 2021 Body Morphometry AI Segmentation Online Challenge**](https://www.kaggle.com/c/body-morphometry-kidney-and-tumor/data)

Real image : 6400장
![데이터 구조](./img/ct1.png)



Fake image : 1333장

dataset_fake![image](https://user-images.githubusercontent.com/65914440/143831332-65a3fa78-e8be-4750-a63f-4f78152b5781.png)
 


## Data pre-processing

- 전체 데이터를 Train dataset(70%), Validation dataset(20%)와 Test dataset(10%)으로  
  분류했다. Fake data가 추가될 경우에는 train dataset에만 포함되도록 했다.
- CT이미지는 신체부위에 따라 WW(Window Width:픽셀값의 범위)와 WL(Window Center:기준이 되는 픽셀값)을 조절해 이미지를 사용합니다. 
  저희는 실험적으로 해보며 학습이 가장 잘되는 WW는 400, WL은 0으로 조정했다.
- 최대-최소 정규화를 했다.
- Segmentation 모델의 예측의 채널은 훈련된 클래스의 갯수와 동일합니다. 
  각각의 채널이 하나의 클래스를 대표한다. 
  모든 클래스를 포함한 Label을 클래스별로 채널을 나눠주는 작업이 필요하다. 
  우리는 하나의 채널로 구성되었던 Label을 2채널로 나누어 0채널은 신장, 1채널에는 종
  양으로 구성했다.  




## Model

### 1.FPN (Pretrained)


### 2. U-net (our Model)

------

## GAN

### Pix2Pix
- make new data to improve CNN acc.


------

## Result

1. real without augmentation
2. real with augmentation
3. real & fake without augmentation
4. real & fake with augmentation


## later work
-sdfsadf

## Data Citation

Nicholas Heller, Niranjan Sathianathen, Arveen Kalapara, Edward Walczak, Keenan Moore, Heather Kaluzniak, Joel Rosenberg, Paul Blake, Zachary Rengel, Makinna Oestreich, Joshua Dean, Michael Tradewell, Aneri Shah, Resha Tejpaul, Zachary Edgerton, Matthew Peterson, Shaneabbas Raza, Subodh Regmi, Nikolaos Papanikolopoulos, Christopher Weight. The kits19 challenge data: 300 kidney tumor cases with clinical context, ct semantic segmentations, and surgical outcomes. arXiv preprint arXiv:1904.00445, 2019. URL https://arxiv.org/abs/1904.00445

## TCIA Citation
Clark K, Vendt B, Smith K, Freymann J, Kirby J, Koppel P, Moore S, Phillips S, Maffitt D, Pringle M, Tarbox L, Prior F. The Cancer Imaging Archive (TCIA): maintaining and operating a public information repository. Journal of Digital Imaging. 2013 Dec;26(6):1045-57. DOI: 10.1007/s10278-013-9622-7

## Data License 

Creative Commons CC-BY-NC-SA license
