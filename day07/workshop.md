# Workshop Day 07

## Problem

### 아래와 같은 Animal 클래스가 있을 때, 해당 클래스를 상속 받아 아래 보기와 같이 동작하는 Dog 클래스와 Bird 클래스를 작성하시오.

```python
class Animal:
    def __init__(self, name):
        self.name = name
        
    def walk(self):
        print(f'{self.name}! 걷는다!')
        
    def eat(self):
        print(f'{self.name}! 먹는다!')
        
```

```python
class Dog(Animal):
    # 생성자는 부모 클래스로부터 받아옵니다.
    def walk(self):  # method overriding
        print(f'{self.name}! 걷지 않고 달린다!')
    def run(self):  # Dog 클래스 만의 메서드
        print(f'{self.name}! 달린다!')

class Bird(Animal):
    # 생성자는 부모 클래스로부터 받아옵니다.
    def fly(self):  # Bird 클래스 만의 메서드
        print(f'{self.name}! 푸드덕!')

```

```python
dog = Dog('바둑이')
dog.walk()
dog.run()

bird = Bird('구구')
bird.walk()
bird.eat()
bird.fly()

'''
바둑이! 걷지 않고 달린다!
바둑이! 달린다!
구구! 걷는다!
구구! 먹는다!
구구! 푸드덕!
'''
```

