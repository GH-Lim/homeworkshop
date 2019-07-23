# Workshop Day 06

## Problem

### 아래와 같은 클래스 Circle이 있을 때, 반지름이 3이고 x, y 좌표가 (2, 4)인 원을 만들어 넓이와 둘레를 출력하시오.
```python
class Circle:
    pi = 3.14
    x = 0
    y = 0
    r = 0
    
    def __init__(self, r, x, y):  # 생성자를 통해 반지름과 x, y 좌표를 받아올 수 있습니다.
        self.r = r
        self.x = x
        self.y = y
        
    def area(self):
        return self.pi * self.r * self.r
    
    def circumference(self):
        return 2 * self.pi * self.r
    
    def center(self):
        return (self.x, self.y)
    
```

```python
my_circle = Circle(3, 2, 4)  # 반지름, x, y 순서

print(f'(x, y) 좌표 : {my_circle.center()}')
print(f'넓이 : {my_circle.area()}')
print(f'둘레 : {my_circle.circumference()}')
'''
출력
(x, y) 좌표 : (2, 4)
넓이 : 28.259999999999998
둘레 : 18.84
'''
```

