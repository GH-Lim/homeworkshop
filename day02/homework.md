# Homework Day02

## 문제 1

### 아래 보기 중, 변경할 수 있는(mutable) 것과 변경 불가능한 것(immutable)을 구분 하시오.
String List Tuple Range Set Dictionary

#### 변경할 수 있는 것

List, Set, Dictionary

#### 변경 불가능한 것

String, Tuple, Range

## 문제 2

### range와 slicing을 활용하여 1부터 50까지 숫자 중 홀수로 이루어진 리스트를 만드시오.
```python
a = list(range(1, 51)) # 1부터 50까지의 숫자를 list로 만듭니다.
b = a[0 : 50 : 2]
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

