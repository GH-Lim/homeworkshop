# Homework Day02

## 문제 1

### 아래 보기 중, 변경할 수 있는(mutable) 것과 변경 불가능한 것(immutable)을 구분 하시오.
String List Tuple Range Set Dictionary

#### 변경할 수 있는 것

List, Set, Dictionary

```python
# List
>>> my_list = [0, 1, 2]
>>> my_list[0]
0
>>> my_list[0] = 3
>>> my_list
[3, 1, 2]			# 아이템에 접근해서 변경 가능 합니다.
```

```python
# Set
>>> my_set
{2, 4, 5}
>>> my_set = my_set - {2}
>>> my_set
{4, 5}				# 아이템을 인덱스를 통해 접근할 순 없지만 변경 가능합니다.
```

```python
# Dictionary
>>> my_dict
{'짜장면': '123'}
>>> my_dict['짜장면'] = '456'
>>> my_dict
{'짜장면': '456'}	# key 값을 통해 value에 접근하여 변경 가능합니다.
```

#### 변경 불가능한 것

String, Tuple, Range

아이템에 접근해서 변경을 시도하면 에러가 발생합니다.

```python
# String
>>> my_str[0] = 'h'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object does not support item assignment

```

```python
# Tuple
>>> my_tuple[0] = 4
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'tuple' object does not support item assignment
```

```python
# Range
>>> my_range[0] = 1
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'range' object does not support item assignment
```



## 문제 2

### range와 slicing을 활용하여 1부터 50까지 숫자 중 홀수로 이루어진 리스트를 만드시오.
```python
a = list(range(1, 51)) # 1부터 50까지의 숫자를 list로 만듭니다.
b = a[0::2] # 마지막 인덱스 까지
# a[0] == 1 이므로 1부터 2씩 증가되는 list를 만들어 홀수로만 이루어진 리스트를 만듭니다.
print(b)
'''
출력
[1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 35, 37, 39, 41, 43, 45, 47, 49]
'''
```

## 문제 3

### 반 학생들의 정보를 이용하여 key는 이름, value는 나이인 딕셔너리를 만드시오.

```python
students_info = {}
students_num = int(input('학생 수를 입력하세요: '))
for i in range(students_num):
    name = input(f'{i+1}번째 학생 이름을 입력하세요: ')
    age = input(f'{i+1}번째 나이를 입력하세요: ')
    students_info[name] = age
print(students_info)
'''
출력
학생 수를 입력하세요: 3
1번째 학생 이름을 입력하세요: 홍길동
1번째 나이를 입력하세요: 27
2번째 학생 이름을 입력하세요: 김철수
2번째 나이를 입력하세요: 28
3번째 학생 이름을 입력하세요: 이영희
3번째 나이를 입력하세요: 26
{'홍길동': '27', '김철수': '28', '이영희': '26'}
'''
```

