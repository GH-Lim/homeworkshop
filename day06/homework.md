# Homework Day 06

## 1번 문제

### Python은 객체 지향 프로그래밍 언어입니다. Python에서 기본적으로 정의되어 있는 클래스 5가지만 작성하시오.
```python
print(type(str))  # <class 'type'>
print(type(int))  # <class 'type'>
print(type(list))  # <class 'type'>
print(type(dict))  # <class 'type'>
print(type(set))  # <class 'type'>
```



## 2번 문제

### 다음 매직 메서드의 역할을 간단하게 작성하시오.

- `__init__`

  인스턴스를 만들 때 호출되는 메서드

- `__del__`

  인스턴스가 소멸될 때 호출되는 메서드

- `__str__`

  인스턴스를 사용자 콘솔창에 출력할 때 호출되는 메서드

- `__repr__`

  인스턴스 자체에 입력되게 하는 메서드

## 3번 문제

### 아래 코드의 ‘.sort()’와 같이 문자열, 리스트, 딕셔너리 등을 조작할 때 사용하였던 것들은 클래스에 정의된 메서드들이었다. 이처럼 문자열, 리스트, 딕셔너리 등을 조작하는 메서드 3가지를 그 역할과 함께 작성하시오.
```python
numbers = [5, 1, 2]
numbers.sort()
print(numbers)  # [1, 2, 5]
```

```python
# 문자열 조작 메서드
my_string = 'Hello World'

my_string.split(' ')  # ['Hello', 'World']
# 문자열을 ' ' (띄어쓰기)를 기준으로 나눠서 리스트에 저장합니다.
```

```python
# 리스트 조작 메서드
my_list = [1, 2, 3]

my_list.append(4)  # [1, 2, 3, 4]
# 리스트 마지막 인덱스에 요소를 추가합니다.
```

```python
# 딕셔너리 조작 메서드
my_dict = {
    '양자강': '차돌짬뽕',
    '김밥카페': '라돈'
}

my_dict.update({'김밥카페': '치즈라면'}) # {'양자강': '차돌짬뽕', '김밥카페': '치즈김밥'}
# 딕셔너리의 key 값에 접근하여 값을 수정하거나 없다면 추가합니다.
```

