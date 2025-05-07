# 소개
해당 레파지토리는 세종대학교 SAI 동아리에서 진행하는 BE 스터디의 개인 코드를 담고 있습니다.  
AI을 활용하여 사람의 감정이나 뇌 상태를 이해하고 분류하는 다양한 주제를 탐구하는 내용을 담고 있습니다.  
그리고 논문을 중심으로 일반적인 머신러닝 및 딥러닝 알고리즘을 직접 구현하고 실습하는 내용을 포함합니다.

# 내용

## 2025_0319_0326 주간 정리
- 개념 정리: CSP (Common Spatial Patterns)  
→ EEG 신호의 공간 패턴을 분리하여 클래스 간 분산을 극대화하는 기법  
  

- 논문 리뷰: A Deep Learning Approach for Motor Imagery EEG Signal Classification  
→ 딥러닝을 활용한 Motor Imagery EEG 분류 모델 제안, 기존 CSP 기반 방법보다 정확도 향상  
## 2025_0327_0402 주간 정리
- 개념 정리: Gaussian Filter  
  → 이미지 분류에서 노이즈를 제거하고 일반화 능력을 올리기 위해 적용,  
  → 하지만 글씨 필체같은 경우는 오히려 방해가 될 수도 있음. 즉, 단순한 구조 분류시에는 유용
  

- 논문 정리: Emotion AI, Real-Time Emotion Detection using CNN  
  → AlexNet을 통해 7~8가지 감정을 분류하는데, LeNet보다 성능이 좋게 나왔음.  
  → 다만, 정성적 평가(눈대중으로 평가) 방식은 눈에 띄게 향상하지 않았음.  
  → 감정분류는 실시간 cv 모듈을 통해 AWS 서버에서 실시간 감정처리 방식으로 진행
## 2025_0403_0409 주간 정리
- 개념 정리1: DCGAN  
  → DCGAN(Deep Convolutional GAN)은 GAN의 한 종류로, Generator와 Discriminator 모두에 CNN 구조를 적용한 모델.  
  → MLP 대신 Conv2D, ConvTranspose2D, BatchNorm 등을 사용하여 이미지 생성을 안정적으로 수행함.  
  → 벤치마크 데이터셋(MNIST, CelebA 등)에서 현실감 있는 이미지를 생성하며, GAN의 대표적인 구현 사례로 활용됨.  
  

- 개념 정리2: CBIR  
  → CBIR(Content-Based Image Retrieval)은 이미지의 메타데이터가 아닌 시각적 내용(색상, 형태, 질감 등)을 기반으로 유사한 이미지를 검색하는 기술.  
  → 특징 벡터를 추출한 뒤, 유클리디안 거리나 코사인 유사도 기반으로 유사 이미지를 반환.  
  → 전통적으로는 색 히스토그램이나 SIFT 같은 방식이 사용되었지만, 최근에는 CNN 기반 특징 추출이 일반적.
  

- 논문 정리: A Visual Similarity Recommendation System using Generative Adversarial Networks  
  → InfoGAN 기반 구조를 사용하여 신발 이미지 간 시각적 유사도를 측정하는 추천 시스템을 제안함.  
  → Discriminator의 중간 출력을 1536차 특징 벡터로 사용하여 MongoDB에 저장, 쿼리 이미지와 유사한 이미지를 L2 거리 기반으로 검색함.  
  → 실험 결과, 제안한 모델이 기존 CNN 모델보다 유사한 이미지 검색 정확도가 높았고, 특히 같은 카테고리 내의 시각적 유사성에서 높은 성능을 보임.

### 2025_0501_0507 주간 정리

- 개념 정리: C50 (Clarity Index at 50ms)
→ C50은 음성 신호에서 **명료도(clarity)**를 수치화한 지표로, 초기 반사음(0~50ms)과 늦은 반사음(50ms 이후) 간 에너지 비율을 로그 스케일로 계산함.  
→ 값이 높을수록 소리가 또렷하고 명확하게 들리며, 낮을수록 잔향이 많아 울리는 느낌을 줌.    
→ TTS 품질 평가나 녹음 환경 개선, 청각 보조 기술 등에서 유용하게 사용됨.    

- 논문 정리: Natural language guidance of high-fidelity text-to-speech with synthetic annotations  
→ 자연어 설명만으로 음성의 스타일, 억양, 채널 품질 등을 직관적으로 제어할 수 있는 고품질 TTS 모델 제안.  
→ 45,000시간의 데이터를 자동 라벨링하여 학습하고, DAC 코덱을 활용해 높은 오디오 품질을 구현함.  
→ C50, SNR 등의 음향적 특성을 자동 추정해 라벨링하고, 이를 자연어로 변환하여 학습에 활용한 점이 인상적임.  
→ 기존 모델(Audiobox) 대비 자연스러움과 명료도 면에서 우수한 성능을 보였고, 일부 경우 원본보다 더 선호되기도 함.  