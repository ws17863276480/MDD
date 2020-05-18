## 1. 

[]: 

## 데이터셋 설명 

Hospital Universiti Sains Malaysia 에서 인간 윤리 위원회가 승인한 실험 설계에 따라 34명의 MDD, 30명의 정상 환자 수집 MDD 환자는 DSM-IV에 따라 우울증 진단 기준 충족된 환자, 약물 효과를 피하기 위해 2주간의 약물 세척 시간을 거침

## 2. 기존 연구 리뷰

### 1. Wajid Mumtaz의 Dataset을 사용한 논문

- Electroencephalogram (EEG)-based computer-aided technique to diagnose major depressive disorder (MDD) 

  []: https://ark1st.tistory.com/52	"블로그"

  

- A deep learning framework for automatic diagnosis of unipolar depression

  []: https://ark1st.tistory.com/53	"블로그"

  

- Imagery Signal-based Deep Learning Method for Prescreening Major Depressive Disorder

  []: https://ark1st.tistory.com/56?category=805279	"블로그"

  

- Classification of Depression Patients and Normal Subjects Based on Electroencephalogram (EEG) Signal  Using Alpha Power and Theta Asymmetry

  []: https://ark1st.tistory.com/55?category=805279	"블로그"

  

- Detection of major depressive disorder using linear and non-linear features from EEG signals

  []: https://ark1st.tistory.com/54?category=805279	"블로그"

  

### 2.타 데이터셋으로 진행된 연구

Automated EEG-based screening of depression using deep convolutional neural network

Depression Detection Using Relative EEG Power Induced by Emotionally Positive Images and a Conformal Kernel Support Vector Machine



## 3. 논문에 대한 방법론 정리

| 논문명                                                       | 데이터 출처                                                  | 데이터 Shape                                                 | 전처리 방법                                                  | 모델                                                         | 성능                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| [Electroencephalogram (EEG)-based computer-aided technique to diagnose major depressive disorder (MDD)](https://www.sciencedirect.com/science/article/pii/S1746809416300866#bib0220) | Hospital Universiti Sains Malaysia 에서 인간 윤리 위원회가 승인한 실험 설계에 따라 34명의 MDD,  30명의 정상 환자 수집 MDD 환자는 DSM-IV에 따라 우울증 진단 기준 충족된 환자, 약물 효과를 피하기 위해 2주간의 약물 세척  시간을 거침 | Hospital Universiti Sains Malaysia 에서 인간 윤리 위원회가 승인한 실험 설계에 따라 34명의 MDD,  30명의 정상 환자 수집 MDD 환자는 DSM-IV에 따라 우울증 진단 기준 충족된 환자, 약물 효과를 피하기 위해 2주간의 약물 세척  시간을 거침 | 1. 노이즈 제거 (MSEC)     2. 특징 추출      1) EC, EO 데이터에서 2분의 epoch 추출      2) 알파 반구간 비대칭      3) 뇌파 스펙트럼 파워     3. 특징 세트 선택      각각의 Feature들마다 AUC 값에 기반한 순위를 매겨 5,  10, 15, 19개의 feature 집단을 생성 | 1. LR     2. SVM     3. NB                                   | (1) 로지스틱 회귀      - (10개의 Feature) 반구형 알파 비대칭 방법이  97.6% 정확도, 96.66% 민감도, 특이도 =  98.5           (2) NB 분류모델     - (5개의 Feature) 반구형 알파 비대칭 방법이 96.8           (3) SVM     - (19개의 Feature) 반구형 알파 비대칭 방법이 98.4 |
| [A deep learning framework for automatic diagnosis of unipolar depression](https://www.sciencedirect.com/science/article/pii/S1386505619307154#!) | Hospital Universiti Sains Malaysia 에서 인간 윤리 위원회가 승인한 실험 설계에 따라 34명의 MDD,  30명의 정상 환자 수집 MDD 환자는 DSM-IV에 따라 우울증 진단 기준 충족된 환자, 약물 효과를 피하기 위해 2주간의 약물 세척  시간을 거침 | Hospital Universiti Sains Malaysia 에서 인간 윤리 위원회가 승인한 실험 설계에 따라 34명의 MDD,  30명의 정상 환자 수집 MDD 환자는 DSM-IV에 따라 우울증 진단 기준 충족된 환자, 약물 효과를 피하기 위해 2주간의 약물 세척  시간을 거침 | 1. 뇌파 노이즈 제거 (MSEC)          2. 전처리     1초의 window length (256 sample) 로 분할     19개의 채널을 가지며, 256sample     (256 , 19) | 1. 1DCNN     2. 1DCNN + LSTM          Adam     Binary cross entropy 손실함수     sigmoid | 1DCNN      EO 데이터 - 19개 채널을 사용하였을 때      acc 98.32      precision = 99.78     recall = 98.34      f-score = 97.65          1DCNN + LSTM     19개 채널 사용 시,     정확도 = 95.97 %,      정밀도 = 99.23 %,      재현율 = 93.67 %      f-score = 95.14 |
| [Detection of major depressive disorder using linear and non-linear features from EEG signals](https://link.springer.com/article/10.1007/s00542-018-4075-z) | Hospital Universiti Sains Malaysia 에서 인간 윤리 위원회가 승인한 실험 설계에 따라 34명의 MDD,  30명의 정상 환자 수집 MDD 환자는 DSM-IV에 따라 우울증 진단 기준 충족된 환자, 약물 효과를 피하기 위해 2주간의 약물 세척  시간을 거침 | Hospital Universiti Sains Malaysia 에서 인간 윤리 위원회가 승인한 실험 설계에 따라 34명의 MDD,  30명의 정상 환자 수집 MDD 환자는 DSM-IV에 따라 우울증 진단 기준 충족된 환자, 약물 효과를 피하기 위해 2주간의 약물 세척  시간을 거침 | 1. 뇌파 노이즈 제거      0.5hz~32hz 신호만 남기고 cut     ICA를 사용하여 눈 깜빡임 제거          2. feature extraction      1) Band Power      델타 (0.5–4Hz), 세타 (4–8Hz), 알파 (8–13Hz) 및 베타 (13–30Hz)      2) 반구형 비대칭      3) 웨이블릿 변환          3. 차원 축소     비선형 분석(웨이블릿)에 있어서 PCA로 차원 축소 | (1) MLPNN      (2) RFBN      (3) LDA      (4) QDA            | 1) 밴드 파워     알파 전력이 MLPNN 에서 acc 91.67을 달성          2) 반구형 비대칭     알파 비대칭에 대한 QDA에서 73.33의 분류 정확도          3) 비선형 Feature     RWE : RBFN , WE : LDA에서 각각 90%의 분류 정확도          4) 조합     RWE와 알파 파워의 조합은 정확도: 93.33  민감도 : 94.44 특이도 87.78을 보여주었다 |
| [Classification of Depression Patients and Normal Subjects Based on Electroencephalogram (EEG) Signal Using Alpha Power and Theta Asymmetry](https://link.springer.com/article/10.1007/s10916-019-1486-z#Bib1) | Hospital Universiti Sains Malaysia 에서 인간 윤리 위원회가 승인한 실험 설계에 따라 34명의 MDD,  30명의 정상 환자 수집 MDD 환자는 DSM-IV에 따라 우울증 진단 기준 충족된 환자, 약물 효과를 피하기 위해 2주간의 약물 세척  시간을 거침 | Hospital Universiti Sains Malaysia 에서 인간 윤리 위원회가 승인한 실험 설계에 따라 34명의 MDD,  30명의 정상 환자 수집 MDD 환자는 DSM-IV에 따라 우울증 진단 기준 충족된 환자, 약물 효과를 피하기 위해 2주간의 약물 세척  시간을 거침 | 1. 뇌파 노이즈 제거      0.5hz~32hz 신호만 남기고 cut     ICA를 사용하여 눈 깜빡임 제거          2. feature extraction      1) Band Power      델타 (0.5–4Hz), 세타 (4–8Hz), 베타  (13–30Hz)     알파1 (8~10.5), 알파2(10.5~13)      2) 반구간 세타 비대칭     - 8개의 feature          3. 데이터 메트릭스 구성     1) 각 밴드파워에 대한 세트     (60, 19) * 5band          2) 알파+세타 비대칭 조합을 위한 세트 (60*27)          3. Feature Selection     MCFS 를 사용해 피쳐 선택 | (1) 로지스틱 회귀     (2) SVM      (3) NB     (4) DT         | 2) 대역 전력 기반     알파 전력 기반 SVM에서 84.50의  ACC     (          3) 조합     알파2 파워와 세타 비대칭의 조합 - SVM에서 88.33의 분류 정확도     ( 특이도 89.41 %      민감도 90.81 %) |
| Imagery Signal-based Deep  Learning Method for Prescreening Major Depressive Disorder | Hospital Universiti Sains Malaysia 에서 인간 윤리 위원회가 승인한 실험 설계에 따라 34명의 MDD,  30명의 정상 환자 수집 MDD 환자는 DSM-IV에 따라 우울증 진단 기준 충족된 환자, 약물 효과를 피하기 위해 2주간의 약물 세척  시간을 거침 | Hospital Universiti Sains Malaysia 에서 인간 윤리 위원회가 승인한 실험 설계에 따라 34명의 MDD,  30명의 정상 환자 수집 MDD 환자는 DSM-IV에 따라 우울증 진단 기준 충족된 환자, 약물 효과를 피하기 위해 2주간의 약물 세척  시간을 거침 | 1. Feature Selection     저채널 장비에서 사용되는 Fp1, Fp2 채널만 사용          2. STFT     3. 스펙트로그램 변환     4. 2채널 스펙트로그램 병합     5. 차원 축소 - 기존 이미지 1/10 | CNN 모델                                                     | val_acc = 0.75      val_loss = 0.3                           |

## 4. 본 논문에서 사용할 방법론

![](https://github.com/ark1st/MDD/blob/master/mdd-diagram.png?raw=true)



#### 4.1. Noise Reduction

전력선 노이즈, 근육 움직임 등의 인공물들은 50Hz 이상의 주파수를 가짐. Low-Pass Filter와 High pass filter를 사용하여 0.5Hz~32Hz의 주파수만 남기고 cut함.

#### 4.2. Feature extraction

Band pass filter를 사용하여 원하는 주파수 대역대만 추출. 1개의 채널(공간)당 4개의 밴드대역대가 존재하게 됨.

![](https://github.com/ark1st/MDD/blob/master/wave.png?raw=true)

#### 4.3. Data Normalization

데이터 세트의 스케일을 맞추기 위해서 data normalization 작업을 시행함. train set 에서 fit 된 scaler로 test set을 정규화함.



#### 4.4. 딥러닝

CNN 모델을 사용함 (현재 모델 Tuning 중)

#### 4.5. 성능평가

confusion matrix에 기반하여 도출된 Accuracy, Recall, Precision, F1-score을 사용하여 성능평가.

![Understanding Confusion Matrix - Towards Data Science](https://miro.medium.com/max/712/1*Z54JgbS4DUwWSknhDCvNTQ.png)



