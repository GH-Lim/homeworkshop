# Homework Day01

## 1 번 문제

### Python 에서 사용할 수 없는 식별자(예약어)를 찾아 작성하세요.

```python
import keyword
print(keyword.kwlist)
```

- keyword 모듈을 불러온 다음 kwlist 메소드를 사용해 확인합니다.

```python
['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
```

## 2 번 문제

### 파이썬에서 float 는 실수를 표현하는 과정에서 같은 값으로 일치되지 않습니다 (floating point rounding error). 따라서, 아래의 값을 비교하기 위해 작성해야하는 코드를 작성하세요
```python
a = 0.1 * 3
b = 0.3
# 일반 비교
print(a == b)				 # 아주 작은 차이가 생기며
					# False 값을 반환합니다.
# 기본적인 처리 방법
print(abs(a - b) <= 1e-10)		# 차이가 아주 작다면 같다고 처리

# sys 모듈을 통해 처리하는 방법
import sys
print(abs(a - b) <= sys.float_info.epsilon)

# math 모듈을 통해 처리하는 방법 (python 3.5부터 활용 가능)
import math
print(math.isclose(a, b))

# 세 방법 모두 True를 출력합니다.
```

## 3 번 문제

### 이스케이프 문자열 중 1) 줄바꿈 2) 탭 3) \ 을 작성하세요.

```python
print(f'줄바꿈은 \\n\n입니다.')
'''
줄바꿈은 \n
입니다.
'''
print(f'탭은 \\t 탭\t탭입니다.')
'''
탭은 \t 탭	탭입니다.
'''
print(f'\\은 \\\\입니다.')
'''
\은 \\입니다.
'''
```

## 4 번 문제

### "안녕, 철수야"를 String Interpolation을 사용하여 출력하세요.

```python
name = '철수'

# %-formatting
print('안녕, %s야' % name)
# str.format()
print('안녕, {}야'.format(name))
# f-string
print(f'안녕, {name}야')
'''
세 결과 모두
안녕, 철수야
출력
'''
```

## 5 번 문제

### 다음 중 형변환시 오류가 발생하는 것은?

```python
# 1)
print(str(1)) # '1'
# 2)
print(int('30')) # 30
# 3)
print(int(5)) # 5
# 4)
print(bool('50')) # True
# 5)
print(int('3.5')) # error
				# int(float('3.5')) 로 바꾼다면 3 을 출력한다.
    			# '3.5'라는 문자열은 float으로 바꿀 수 있지만
        		# int형으로 바로 바꾸지 못한다.
```

정답 5번