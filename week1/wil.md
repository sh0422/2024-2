//C311031 김시훈 과제1
[퀴즈1]
다음 중 학습방법에 대한 설명으로 가장 적절하지 않은 것은??
- (1) 준지도학습은 레이블이 지정된 데이터와 지정되지 않은 데이터를 모두 활용한다.
- (2) 준지도학습은 적은 양의 레이블된 데이터로 모델의 성능을 향상시킬 수 있다.
- (3) 비지도학습은 외부 레이블 없이 데이터 자체에서 감독 신호를 생성한다.
- (4) 준지도학습은 지도학습과 비지도학습의 중간 형태로 볼 수 있다.
- (5) 지도학습(Supervised Learning)의 한계점으로 고품질의 레이블된 데이터를 대량으로 확보하기 어렵고 비용이 많이 든다는 점이 있다.
[정답1]
(3)



[퀴즈2]
XOR 문제를 단일 퍼셉트론으로 해결할 수 없는 이유는 무엇인가요??
[정답2]
(선을 그어 구분하는 것으로 xor 문제 해결 불가능)



[코딩3]
퍼셉트론 구현: ans1과 ans2를 숫자로 변경하시오.
import numpy as np
def Perceptron(x, w, b):
    y = np.sum(w * x) + b
    if y <= 0:
        ans1 = "빈칸 1" # 숫자(int)로 변경하시오
        return ans1
    else:
        ans2 = "빈칸 2" # 숫자(int)로 변경하시오
        return ans2 
# NAND 게이트
def NAND(x1, x2):
    return Perceptron(np.array([x1, x2]), np.array([-0.5, -0.5]), 0.7)
# OR 게이트
def OR(x1, x2):
    return Perceptron(np.array([x1, x2]), np.array([0.5, 0.5]), -0.2)
# AND 게이트
def AND(x1, x2):
    return Perceptron(np.array([x1, x2]), np.array([0.5, 0.5]), -0.7)
# 테스트
print("NAND 게이트:")
print(NAND(0, 0), NAND(0, 1), NAND(1, 0), NAND(1, 1))
print("OR 게이트:")
print(OR(0, 0), OR(0, 1), OR(1, 0), OR(1, 1))
print("AND 게이트:")
print(AND(0, 0), AND(0, 1), AND(1, 0), AND(1, 1))
[정답3]
ans1 = (0), ans2 = (1)



[설문]
다음 보기 중, 본인이 설명할 줄 아는 키워드를 모두 고르시오?
- (1) 검증 데이터셋과 테스트 데이터셋
- (2) 과적합과 과소적합
- (3) 활성화함수
- (4) 앙상블 학습
- (5) 오토인코더
- (6) 전이학습
- (7) 어텐션 메커니즘
[해설]
(6)