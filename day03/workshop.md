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