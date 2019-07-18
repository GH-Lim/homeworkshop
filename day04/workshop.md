# Workshop Day04

## 문제

### 양의 정수 x를 입력 받아 제곱근의 근사값을 반환하는 함수를 작성하세요. sqrt() 사용 금지

```python
def approx_sqrt(number, times):
    max_num = number  # 입력받은 숫자를 최대값
    min_num = number - 1  # 입력받은 숫자 - 1 을 최소값에 넣습니다.
    for i in range(times): # 입력받은 반복 횟수 만큼 이분법을 시행 합니다.
        if ((max_num + min_num) / 2) ** 2 > number: # 최대값 + 최소값 / 2 의 제곱이 입력받은 수
            max_num = ((max_num + min_num) / 2)     # number 보다 크다면 최대값에 (최대값 + 최소값) / 2
        else:
            min_num = ((max_num + min_num) / 2)     # number 보다 작다면 최소값에 (최대값 + 최소값) / 2
    print(f'''
    {min_num} < sqrt({number}) < {max_num}
    ''')
    return (max_num + min_num) / 2 # 최대값과 최소값의 절반을 근사값으로 반환합니다.
num = int(input('양의 정수를 입력하세요: '))
time = int(input('이분법을 반복할 횟수: '))

result = approx_sqrt(num, time)
print(f'sqrt({num})의 근사값은 {result}입니다.')

'''
출력
양의 정수를 입력하세요: 2
이분법을 반복할 횟수: 11

    1.4140625 < sqrt(2) < 1.41455078125

sqrt(2)의 근사값은 1.414306640625입니다.
'''
```

