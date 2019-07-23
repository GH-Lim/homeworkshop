# Homework Day 05

```python
def fibo_recursion(n):
    if n < 2:
        return n
    else:
        return fibo_recursion(n-1) + fibo_recursion(n-2)

```

## 1. 위와 같은 코드가 fibo.py 파일에 작성되어 있을 때, 아래와 같이 함수를 실행할 수 있도록 하는 import 구문을 (A), (B), (C)를 채워 넣어 완성하시오.

```python
from fibo import fibo_recursion as recursion

print(recursion(4))
'''
출력
3
####
1 1 2 3 5 8 ...
      ^
정상적으로 출력되는 것을 볼 수 있습니다.
'''
```

## 2. 다음 에러들이 어떠한 경우에 발생하는지 간단하게 작성하시오.

- ZeroDivisionError

  숫자를 0으로 나눌 때 발생합니다.

  ```python
  10 * 1 / 0
  '''
      10 * 1 / 0
  ZeroDivisionError: division by zero
  '''
  ```
  
- NameError

  정의되지 않은 변수를 호출 할 때 발생합니다.

  ```python
  print(name)
  '''
      print(name)
  NameError: name 'name' is not defined
  '''
  ```

  

- TypeError

  1) 자료형의 타입이 잘못 되었을 때

  2) 함수 호출 시 정의되지 않은 타입을 입력했을 때

  3) 함수 호출 시 필수 argument를 누락했을 때

  4) 함수 호출 시 argument를 많이 입력했을 때

  등의 상황에서 발생 합니다.

  ```python
  1 + '1'
  '''
      1 + '1'
  TypeError: unsupported operand type(s) for +: 'int' and 'str'
  '''
  
  round('3.5')
  '''
      round('3.5')
  TypeError: type str doesn't define __round__ method
  '''
  
  import random
  random.sample([1, 2, 3])
  '''
      random.sample([1, 2, 3])
  TypeError: sample() missing 1 required positional argument: 'k'
  '''
  random.sample([1, 2, 3], 1, 2)
  '''
      random.sample([1, 2, 3], 1, 2)
  TypeError: sample() takes 3 positional arguments but 4 were given
  '''
  ```

  

- IndexError

  범위를 벗어난 인덱스를 호출할 때 발생합니다.

  ```python
  numbers = [1, 2]
  numbers[3]
  '''
      numbers[3]
  IndexError: list index out of range
  '''
  ```

  

- KeyError

  해당 딕셔너리에 존재하지 않는 key값을 호출할 때 발생합니다.

  ```python
  lunch = {'양자강': '차돌짬뽕'}
  lunch['김밥카페']
  '''
      lunch['김밥카페']
  KeyError: '김밥카페'
  '''
  ```

  

- ModuleNotFoundError

  import 한 모듈을 찾을 수 없을 때 발생합니다.

  ```python
  import reque
  '''
      import reque
  ModuleNotFoundError: No module named 'reque'
  '''
  ```
  

  
- ImportError

  불러온 모듈에서 함수이름을 찾을 수 없을 때 발생합니다.
  
  ```python
from bs4 import BS
  '''
      from bs4 import BS
  ImportError: cannot import name 'BS' from 'bs4' (C:\Users\student\AppData\Local\Programs\Python\Python37\lib\site-packages\bs4\__init__.py)
  '''
  ```
  
  