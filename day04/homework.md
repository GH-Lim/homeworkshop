# Homework Day04

## 1 번 문제

### Python에서 변수를 찾을 때 접근하는 이름 공간을 순서대로 작성하시오.

LEGB

`Local scope` : 정의된 함수

`Enclosed scope` : 상위 함수

`Global scope` : 함수 밖의 변수 혹은 import된 모듈

`Built-in scope` : 파이썬안에 내장되어 있는 함수 또는 속성

```python
import random

lecturer = 'Jason'

def greeting(name):
    value = '안녕하세요'
    
    def greeting2(age):
        random.random() # random은 import된 모듈 'Global scope'
        print(lecturer) # lecturer는 함수 밖의 변수 'Global scope'
        print(str(age)) # str은 파이썬에 내장된 함수 'Built-in scope'
        			   # age는 함수에서 정의된 변수 'Local scope'
        print(value)  # value는 상위 함수의 변수 'Enclosed scope'
    
    greeting2(6)
    
    message = f'{name}님 {value}'  # Local Scope
    print(message)
    
greeting('홍길동')
```

## 2 번 문제

### 다음 중 옳지 않은 것을 고르시오.

1. 함수는 오직 하나의 객체만 반환할 수 있어서, ‘return a, b’처럼 쓸 수 없다. ===> (X) 쓸 수 있다.

   ```python
   def test():
       a = 1
       b = 2
       return a, b
   
   print(test())
   '''
   출력 # 튜플 형태의 하나의 객체로 반환된다.
   (1, 2)
   '''
   ```

   

2. 함수에서 return을 작성하지 않으면 None 값을 반환한다.

   ```python
   def test():
       a = 1
       b = 2
   #    return a, b
   
   print(test())
   '''
   출력 # 리턴 값이 없어 None 반환
   None
   '''
   ```

   

3. 함수의 인자(parameter)는 함수를 선언할 때 설정한 값이며, 인수(argument)는 함수를 호출할 때 넘겨주는 값이다.

   ```python
   def my_func(*args, second_arg='2nd'): # parameters 매개변수
       print(args)
       print(type(args))
       print(second_arg)
   my_func(123, 444, 2, 12, 45, second_arg='1st') # arguments 전달인자
   ```

   

4. 가변 인자를 설정할 때는 인자 앞에 *을 붙이고, 이 때는 함수 내에서 tuple로 처리된다.

   ```python
   def my_func(*args, second_arg='2nd'):
       print(args)
       print(type(args))
       print(second_arg)
   my_func(123, 444, 2, 12, 45, second_arg='1st')
   '''
   출력 # 가변인자 args 의 type 은 tuple 이다.
   (123, 444, 2, 12, 45)
   <class 'tuple'>
   1st
   '''
   ```

   

## 3 번 문제

### 재귀 함수를 쓰는 장점과 단점을 작성하시오.

```python
# 재귀함수
def fib(n):
    return fib(n - 1) + fib(n - 2) if n > 1 else 1
fib(4)
```



```python
# 반복문
def fib_loop(n):
    result = [1, 1]
    for i in range(1, n):
        result.append(result[-2] + result[-1])
    print(result)
    return result[-1]

fib_loop(10)
```

#### 장점

1. 위와 같은 피보나치 수를 반환하는 함수를 선언할 때, 알고리즘 적으로 직관적인 표현이 가능합니다.
2. 변수의 사용을 줄일 수 있습니다.

#### 단점

1. 스택을 소비하여 함수 호출 횟수가 많아지면 루프를 사용한 함수보다 속도가 현저히 느려집니다.
2. 베이스 케이스, 리턴값 계산 등이 어렵다.
3. 메모리를 많이 사용한다. (파이썬은 1000번 째 재귀를 받으면 오류 발생)