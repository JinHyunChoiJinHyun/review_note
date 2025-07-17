# 최소공배수 반환 문제

## 문제 설명

- 배열에 존재하는 요소들의 최소공배수 반환

## 입력 예시 
 ```python
 arr = [2,6,8,14]	
 arr = [1,2,3]	 
 ```

# 실패한 이유
- 최소 공약수 계산 함수 모름

# 해결 아이디어
1. 최소 공약수 반환 함수 작성
2. 배열의 앞부터 숫자를 하나씩 누적하며 두 수의 최소 공배수 반환

``` python
import math
def lcm(a,b): 
    return a * b // math.gcd(a,b) # 두 수의 곱을 최대 공약수로 나눔

def solution(arr):
    result = arr[0]
    for num in arr[1:]:
        result = lcm(result, num)
    
    return result
```

# 복잡도 계산

## 시간 복잡도 
1. math.gcd => 유클리드 호제법 기반
-> O(n log M)

=> 총 O(n log M)


