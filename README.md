# AI 자율주행
### 차선인식
0. 학습 데이터: AI-HUB
1. 전처리(데이터): GrayScale
2. 학습모델: Canny Edge Detection (확실한 엣지로 판단되는 부분만 남겨짐)
   1. 노이즈 제거 (Gaussian 필터링)
   2. Gradient 값이 높은 부분 찾기(Gradient방향은 엣지에서 수직)
   3. 최대값이 아닌 픽셀을 0으로 만듬
   4. Hyteresis Thresholding(3단계까지 거친것이 실제 엣지인지 판단)
      - 문턱값을 minValue, maxValue로 잡아 maxValue보다 높으면 확실한 엣지값, minValue보다 적으면 엣지에서 제외
   
3. 추론

**참고: https://medium.com/@mrhwick/simple-lane-detection-with-opencv-bfeb6ae54ec0
### 번호판 인식