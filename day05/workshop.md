# Workshop Day 05

## Problem

### 1. 2개의 숫자를 인자로 받아 더하기, 빼기, 곱하기, 나누기 연산의 결과를 반환하는 4개의 함수를 calc.py에 작성하시오. 단, 나누기 연산에서는 try except 구문을 사용하여 ‘0’으로 나누려고 하는 경우에는 문자열 ’0으로는 나눌 수 없습니다.’을 반환하시오.

```python
## calc.py
def my_sum(num1, num2):
    return num1 + num2 # 더하기

def my_sub(num1, num2):
    return num1 - num2 # 빼기

def my_mul(num1, num2):
    return num1 * num2 # 곱하기

def my_div(num1, num2):
    try:
        return num1 / num2 # 나누기
    except ZeroDivisionError:
        return '0으로는 나눌 수 없습니다.' # ZeroDivisionError
    
```

### 2. 1번에서 작성한 calc.py 모듈을 import하여, 각 연산을 수행하는 함수들을 실행하는 코드를 작성하시오.
```python
## workshop.py
import calc # calc.py 모듈 import

print(calc.my_sum(3, 1)) # 더하기
print(calc.my_sub(3, 1)) # 빼기
print(calc.my_mul(3, 2)) # 곱하기
print(calc.my_div(5, 2)) # 나누기
print(calc.my_div(2, 0)) # ZeroDivision

'''
출력 결과
4						# 3 + 1
2						# 3 - 1
6						# 3 * 2
2.5						# 5 / 2
0으로는 나눌 수 없습니다.	  # 2 / 0
'''
```

