# Numpy
- 파이썬에서 계산을 빠르게 하기 위한 라이브러리
- 빠른 연산 속도, 다양한 수학, N차원 배역 객체(ndarray)를 지원
- $ pip inatall numpy 명령어로 설치 후 사용
```python
import numpy as np
import time

n = 1_000_000

# 파이썬 리스트
py_list = list(range(n))

result_list = [x * 2 for x in py_list]  # 0.042010 초


# NumPy 배열
np_array = np.arange(n)

result_array = np_array * 2   # 0.000779 초

# 약 50배 정도 빠름 
```
### ndarray
- N-dimensional array
- 대규모 숫자 데이터를 빠르고 효율적으로 처리하기 위해 만들어진 특수한 데이터 구조이다.
- 모든 원소를 하나의 연속된 메모리 공간에 저장한다. (like c)
- 내부의 모든 원소들은 반드시 같은 데이터 타입을 가져야 한다.
- N-차원 등 원하는 만큼의 차원을 직관적으로 표현하고 다룰 수 있다.
- 머신러닝에서의 Pandas, TensorFlow, PyTorch와 같은 다른 라이브러리들의 기반이 되는 핵심 데이터 구조이다.
- 배열 자체에 대한 중요한 정보들을 속성으로 가지고 있음
  - .ndim : 배열의 차원수
  - .shape : 각 차원의 크기
  - .size : 전체 원소의 개수
  - .dtype : 원소의 데이터 타입

```python
import numpy as np

data = [[1, 2, 3],
        [4, 5, 6]]

arr = np.array(data)

print(arr, '\n')

print(f"차원: {arr.ndim}")
print(f"모양: {arr.shape}")
print(f"원소 개수: {arr.size}")
print(f"데이터 타입: {arr.dtype}")
```
```
[[1 2 3]
 [4 5 6]] 

차원: 2
모양: (2, 3)
원소 개수: 6
데이터 타입: int64
```
## numpy 함수
- 직접적으로 값을 입력해 배열을 만드는 방식 외에 다양한 생성 함수를 제공함
- np.zeros() : 모든 원소가 0으로채워진배열을생성, 주로 배열의 틀을 미리만들고 나중에 값을 채우는 용도로 사용
- np.ones() : 모든 원소가 1로 채워진 배열을 생성, 초기화, 효율적인 수학 연산을 위한 용도로 사용
- np.full(shape, fill_value) : 지정한 모양의 배열을 만들고, 모든 요소를 지정한 값으로 채워줌
- np.arrange() : 연속적인 숫자 배열 생성, 파이썬의 range()와 동일하게 동작하되, 결과를 ndarray로 반환한다.
- np.linspace() : 시작점부터 끝점까지 지정한 개수만큼 균일한 간격의 배열 생성, 주로 데이터 시각화, 함수 계산, 머신러닝 알고리즘에서 사용
## 인덱싱과 슬라이싱
- 1차원 배열 : 파이썬 리스트와 사용법이 완전히 동일
- 2차원 배열 : [행, 열]의 형태로 접근하여 특정 위치의 요소를 선택, 파이썬 리스트처럼 [행][열]의 형태로도 접근할 수 있지만, 표준이 아니며 비효율적이다.
## numpy 연산
## numpy 집계 함수

# Pandas
## Inspecting
## indexing & filtering

# 데이터 전처리 및 변환

# AI 기초 수학
## 지수함수
## 미분
## 벡터와 내적
## 통계 기초