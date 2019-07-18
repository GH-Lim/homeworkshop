# Workshop Day03

### Palindrome은 앞에서부터 읽었을 때와 뒤에서부터 읽었을 때 같은 단어를 뜻한다. 따라서, 'a' 'nan' '토마토' 모두 palindrome에 해당합니다. 단어를 입력받아 Palindrome을 검증하고 True나 False를 리턴하는 함수 palindrome(word)를 만들어보세요.
```python
def palindrome(word):
    reverse_word = '' # 빈 string을 선언합니다.
    for i in range(len(word)):
        reverse_word += word[len(word)-i-1]  # 빈 string에 word를 뒤에서부터 입력합니다.
    if word == reverse_word:
        return True  # 같다면 True를 반환합니다.
    else:
        return False # 다르다면 False를 반환합니다.
# return True if word == reverse_word else False  # 리턴 한줄로 가능!
user_word = input()

print(f'''
{user_word}는 Palindrome이 {'맞습니다.' if palindrome(user_word) else '아닙니다.'}
''')


'''
출력1
토마토

토마토는 Palindrome이 맞습니다.

출력2
tomato

tomato는 Palindrome이 아닙니다.
'''

```



```python
# 반장님 풀이 
# reversed 를 사용한 풀이
def palindrome(word):
    return True if list(word) == list(reversed((word))) else False

# CA님 풀이
def palindrome(word)
    a = list(word)
    b = list(reversed(a))
    if b == a:
        print(True)
    else:
        print(False)
```

```python
# Lecturer's Solution #1
# for문을 이용한 풀이
def palindrome(word):
    list_word = list(word) # 5 => 2 | 4 => 2 홀수 이면 중간을 제외한 캐릭터만
    for i in range(len(list_word) // 2): # 몫을 구한다.
        if list_word[i] != list_word[-i-1]: # 앞에서부터와 뒤에서부터의 char를 하나씩 비교
            return False
    return True  # 끝까지 돌아서 다른 것이 없다면 True를 리턴한다.

# Sol #2
# 슬라이싱을 이용한 풀이
def palindrome(word):
    return word == word[::-1] # 기러기 == 기러기 ?? True
```

