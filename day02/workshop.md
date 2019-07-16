# Workshop Day02

## 문제 1

### 두 개의 정수 n과 m이 주어질 때, 반복문을 사용하여 별(*) 문자를 이용해 가로의 길이가 n, 세로의 길이가 m인 사각형을 출력하시오.

```python
# 문제1
n, m = 5, 9
for i in range(n):
    print('*' * m)
'''
출력
*********
*********
*********
*********
*********
'''
```

## 문제2

### 과목명과 점수가 담긴 딕셔너리가 있을 때, 평균 점수를 출력하시오.

```python
# 문제2
student = {'python': 80, 'algorithm': 99, 'django': 89, 'flask': 83}
total_score = 0
for score in student.values():
    total_score += score			# value 를 이용해 총합을 구합니다.
avg_score = total_score / len(student) # 딕셔너리의 길이로 나눕니다.
print(avg_score)
'''
출력
87.75
'''
```



## 문제3

### 다음은 여러 사람의 혈액형(A, B, AB, O)에 대한 데이터이다. 반복문을 사용하여 key는 혈액형의 종류, value는 인원 수인 딕셔너리를 만들고 출력하시오.

```python
# 문제3
blood_types = ['A', 'B', 'A', 'O', 'AB', 'AB', 'O', 'A', 'B', 'O', 'B', 'AB']

bloods_people = {
    'A': 0,
    'B': 0,
    'AB': 0,
    'O': 0,
}				# 딕셔너리의 값들을 0으로 초기화 합니다.

for blood in blood_types:
    bloods_people[blood] += 1 # 해당 혈액형일 때 +1을 합니다.

print(bloods_people)
'''
출력
{'A': 3, 'B': 3, 'AB': 3, 'O': 3}
'''
```

