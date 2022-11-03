wochae
```py
// code
```
nheo
```py
def solution(s):
    return s.count('p') + s.count('P') == s.count('y') + s.count('Y')
```
donghyuk
```py
def solution(s):
    s = s.upper()
    return s.count('P') == s.count('Y')
```
hakim
```py
def solution(s):
    return s.lower().count('p') == s.lower().count('y')
```
