# Test 모델을 이용한 Test 도출

* Github Url: https://github.com/shiny0510/FewShot_GAN-Unet3D (꼭! 하이퍼링크)

* requirement: pandas, numpy, torch, seaborn, matplotlib

1. 수행 기관: 알파코, 빅데이터기반 딥러닝 부트캠프 (역할: Method 튜닝, 전처리, 팀장, 트러블 슈팅)

2. 데이터: 환자 데이터 10000개, 정상인 데이터 20만개

3. Method:  전처리: 이미지 Normalize + MixUp(Augmentation) + Denosing               
            모델: F-AnoGAN (Medical Image Analysis, 2019.05)
	         optimizer: Adam 
            loss: L1 loss
	<img src="https://user-images.githubusercontent.com/85111065/173891979-c4353c43-345f-4cec-8a4f-d818e00d97f5.png" width="500">

4. 결과: <br>

* Anomaly detection: <br>
	<img src="https://user-images.githubusercontent.com/85111065/173892034-27a00459-f7af-4ed7-877c-45baa59f2a10.png" width="500" >

* Acc: <br>
	<img src="https://user-images.githubusercontent.com/85111065/173892050-d0406ab4-e31b-43c1-bfa7-cd121428e1aa.png" width="500" >

* 프로젝트 수행 중 문제: 정상인 데이터에서도 미세한 Anomaly가 검출되어서, 환자로 분류하는 threshold를
    높혀줌으로써 정확히 분류될 수 있도록 조치하였으며, 데이터가 부족하여 오픈데이터를 다수 활용.

5. 참고: Schlegl, Thomas, et al. "f-AnoGAN: Fast unsupervised anomaly detection with generative 
    adversarial networks." Medical image analysis 54 (2019): 30-44.
![test1](https://user-images.githubusercontent.com/85111065/178384059-d80cb24c-bed1-403b-84ae-66ed60c9f397.PNG)
