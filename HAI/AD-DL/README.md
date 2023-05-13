# Convolutional neural networks for classification of Alzheimer's disease: Overview and reproducible evaluation
by aramis-lab  

📚 [paper](https://www.sciencedirect.com/science/article/abs/pii/S1361841520300591?via%3Dihub)  
👩🏻‍💻 [github](https://github.com/aramis-lab/AD-DL/tree/initial/clinicadl/clinicadl)
***
1. ROI-based method & AutoEncoder & Single-CNN 구현  
   - ROI crop 영역을 왼쪽 센터 기준으로 일괄 통일
<br>

2. ROI-based method & AutoEncoder & Single-CNN 보충   
   - 1에서 validation set 수를 77개 → 57개로 줄이고 20개를 test set으로 사용
   - epoch 100 중 50번까지는 필수 실행, 50 이후부터는 patience 5로 EarlyStopping 적용
   - epoch 25마다 모델 저장  
   +) patch size : (50, 50, 50) → (100, 100, 100)  
   +) patch로 자르지 않고 전체 데이터를 사용하여 모델 학습
