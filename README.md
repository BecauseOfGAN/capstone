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

데이터는 

![데이터 구조](./img/ct1.png)




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
