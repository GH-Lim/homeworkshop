# Homework Day 07

## Problem

### 다음은 더하기 기능만이 구현된 간단한 Calculator 클래스이다.

```python
class Calculator:
    count = 0
    
    def info(self):
        print('나는 계산기 입니다.')
    
    @staticmethod
    def add(a,b):
        Calculator.count += 1
        print(f'{a} + {b} 는 {a+b} 입니다.')
        
    @classmethod
    def history(cls):
        print(f'총 {cls.count}번 계산 했습니다.')
        
```

#### 1번. 인스턴스 메서드, 스태틱 메서드, 클래스 메서드에 해당 하는 함수가 무엇인지 작성하시오.

1. 인스턴스 메서드
   - 인스턴스가 할 행동은 모두 인스턴스 메서드로 한정 지어서 설계합니다.

```python
# 인스턴스 메서드 : 인스턴스가 사용할 메서드
# 데코레이터가 없으므로 자동으로 인스턴스 메서드가 됩니다.
# 첫 번째 인자로 self 를 받고 자동으로 인스턴스 객체가 self 가 됩니다.
def info(self):
    print('나는 계산기 입니다.')
```

2. 스태틱 메서드
   - 클래스와 클래스 속성에 접근할 필요가 없다면 스태틱 메서드로 정의합니다.

```python
# 스태틱 메서드 : 클래스가 사용할 메서드
# 정의 위에 @staticmethod 데코레이터를 사용합니다.
# 묵시적인 첫 번째 인자를 받지 않습니다. 인자는 자유롭게 정의합니다.
# 어떠한 인자도 자동으로 넘어가지 않습니다.
@staticmethod
def add(a,b):
    Calculator.count += 1
    print(f'{a} + {b} 는 {a+b} 입니다.')
```

3. 클래스 메서드
   - 클래스 자체(`cls`)와 그 속성에 접근할 필요가 있다면 클래스 메서드로 정의합니다.

```python
# 클래스 메서드 : 클래스가 사용할 메서드
# 정의 위에 @classmethod 데코레이터를 사용합니다.
# 첫 번째 인자로 cls 를 받고 자동으로 클래스 객체가 cls 가 됩니다.
@classmethod
def history(cls):
    print(f'총 {cls.count}번 계산 했습니다.')
```

#### 2번. 각각의 함수(메서드)를 실행하는 코드를 작성하시오.

1. 인스턴스 메서드
   - 클래스도 인스턴스 메서드에 접근 가능하지만 호출하지 않아야 합니다.

```python
calc = Calculator()

calc.info()
Calculator.info(calc)  # 클래스로 인스턴스 메서드 접근. self 값에 calc 를 전달합니다.
'''
나는 계산기 입니다.
나는 계산기 입니다.
'''
```

```python
# 클래스로 접근 시 self 값에 아무 값도 전달하지 않으면
# 자동으로 self 에 넘어갈 인자가 없으므로 TypeError 가 발생합니다.
Calculator.info()
'''
    Calculator.info()
TypeError: info() missing 1 required positional argument: 'self'
'''
```

2. 스태틱 메서드
   - 인스턴스도 스태틱 메서드에 접근 가능하지만 호출하지 않아야 합니다.

```python
calc.add(1, 2)  # 인스턴스로 스태틱 메서드 접근
Calculator.add(1, 2)
'''
1 + 2 는 3 입니다.
1 + 2 는 3 입니다.
'''
```

3. 클래스 메서드
   - 인스턴스도 클래스 메서드에 접근 가능하지만 호출하지 않아야 합니다.

```python
calc.history()  # 인스턴스로 클래스 메서드 접근
Calculator.history()
'''
총 2번 계산 했습니다.
총 2번 계산 했습니다.
'''
```

#### 3번. 파라미터 `self`와 `cls`에는 어떤 값이 할당 되는지 작성하시오.

1. `self`
   - 인스턴스 메서드에 인스턴스로 접근했을 경우 자동으로 인스턴스 객체가 self 가 됩니다.
   - 클래스로 접근했을 경우 자동으로 넘겨줄 값이 없으므로 `Calculator.info(calc)`와 같이 수동으로 넘겨주면 정상적으로 작동하지만 사용하지 않아야 합니다.

2. `cls`
   - 클래스 메서드에 접근한 인스턴스나 클래스 객체가 self 가 됩니다.
   - 인스턴스로 접근했을 경우 정상적으로 작동하지만 사용하지 않아야 합니다.

