# Homework Day03

## 1 번 문제

### Python에서 기본으로 사용할 수 있는 Built in function 5개를 찾아서 작성하세요.

자주 쓰는 5가지

```python
print('Hi') # 출력해주는 함수
sum(1, 5) # 변수들을 더해주는 함수
input('입력하세요:') # 사용자로부터 입력을 받게 해주는 함수
range(10) # range 타입으로 범위를 만들어주는 함수
dict() # 딕셔너리 타입을 생성해주는 함수
```

`dir(__builtins__)` 를 통해 빌트 인 함수를 확인 할 수 있습니다.

```python
print(dir(__builtins__))
'''
['ArithmeticError', 'AssertionError', 'AttributeError', 'BaseException', 'BlockingIOError', 'BrokenPipeError', 'BufferError', 'BytesWarning', 'ChildProcessError', 'ConnectionAbortedError', 'ConnectionError', 'ConnectionRefusedError', 'ConnectionResetError', 'DeprecationWarning', 'EOFError', 'Ellipsis', 'EnvironmentError', 'Exception', 'False', 'FileExistsError', 'FileNotFoundError', 'FloatingPointError', 'FutureWarning', 'GeneratorExit', 'IOError', 'ImportError', 'ImportWarning', 'IndentationError', 'IndexError', 'InterruptedError', 'IsADirectoryError', 'KeyError', 'KeyboardInterrupt', 'LookupError', 'MemoryError', 'ModuleNotFoundError', 'NameError', 'None', 'NotADirectoryError', 'NotImplemented', 'NotImplementedError', 'OSError', 'OverflowError', 'PendingDeprecationWarning', 'PermissionError', 'ProcessLookupError', 'RecursionError', 'ReferenceError', 'ResourceWarning', 'RuntimeError', 'RuntimeWarning', 'StopAsyncIteration', 'StopIteration', 'SyntaxError', 'SyntaxWarning', 'SystemError', 'SystemExit', 'TabError', 'TimeoutError', 'True', 'TypeError', 'UnboundLocalError', 'UnicodeDecodeError', 'UnicodeEncodeError', 'UnicodeError', 'UnicodeTranslateError', 'UnicodeWarning', 'UserWarning', 'ValueError', 'Warning', 'WindowsError', 'ZeroDivisionError', '__build_class__', '__debug__', '__doc__', '__import__', '__loader__', '__name__', '__package__',
'__spec__', 'abs', 'all', 'any', 'ascii', 'bin', 'bool', 'breakpoint', 'bytearray', 'bytes', 'callable', 'chr', 'classmethod', 'compile', 'complex', 'copyright', 'credits', 'delattr', 'dict', 'dir', 'divmod', 'enumerate', 'eval', 'exec', 'exit', 'filter', 'float', 'format', 'frozenset', 'getattr', 'globals', 'hasattr', 'hash', 'help', 'hex', 'id', 'input', 'int', 'isinstance', 'issubclass', 'iter', 'len', 'license', 'list', 'locals', 'map', 'max', 'memoryview', 'min', 'next', 'object', 'oct', 'open', 'ord', 'pow', 'print', 'property', 'quit', 'range', 'repr', 'reversed', 'round', 'set', 'setattr', 'slice', 'sorted', 'staticmethod', 'str', 'sum', 'super', 'tuple', 'type', 'vars', 'zip']
'''
```

## 2 번 문제

### 다음과 같이 함수가 정의되어 있다. 보기 중, 오류가 발생하는 코드를 고르시오.

3 번 !

```python
def ssafy(name, location='서울'):
    print(f'{name}의 지역은 {location}입니다.')
```

1. 오류 없이 실행

   키워드 인자를 통해 직접적으로 특정 인자를 전달할 수 있습니다.

```python
ssafy(location='대전', name='철수')
'''
철수의 지역은 대전입니다.
'''
```

2. 오류 없이 실행

   함수는 기본적으로 인수를 위치로 파악하기 때문에 '길동'을 name에 전달합니다.

```python
ssafy('길동', location='광주')
'''
길동의 지역은 광주입니다.
'''
```

3. 오류 발생

   키워드 인자를 활용한 뒤에 위치 인자를 사용할 수는 없기 때문에 오류가 발생합니다.

```python
ssafy(name='허준', '구미')
'''
    ssafy(name='허준', '구미')
                        ^
SyntaxError: positional argument follows keyword argument
'''
```

4. 질문사항

   name 인자에 여러개의 value가 들어가 TypeError 가 발생합니다.

```python
ssafy('구미', name='허준')
'''
    ssafy('구미', name='허준')
TypeError: ssafy() got multiple values for argument 'name'
'''
```



## 3 번 문제

### 다음과 같이 코드가 작성되어 있을 때, 변수 result에 저장된 값을 작성하시오.

```python
def my_func(a, b):
    c = a + b
    print(c)

result = my_func(4,7)
'''
실행결과
11
'''
```

실행 결과 11이 나와 result 안에 11이 저장 되어있는 것 처럼 보이지만, 실제로는 `my_func(a, b)` 함수 안에 있는 `print(c)`로 인해 11의 값이 출력되는 것입니다.

`my_func` 함수는 `return` 하고 있는 값이 없기 때문에 `None`을 반환합니다. 

따라서, 변수 `result`에는 `None` 상태가 저장되었습니다.

```python
print(result)
'''
11		=> result = my_func(4, 7)을 수행하며 함수 안에 있는 print(c)에 의해 출력되었습니다.
None     => print(result) 가 수행되며 result안에 저장된 값이 출력되었습니다.
'''
```

