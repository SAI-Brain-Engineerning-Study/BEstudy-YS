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