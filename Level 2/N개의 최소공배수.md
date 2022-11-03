wochae
```py
// code
```
nheo
```py
def solution(arr):
    answer = 1
    nums = [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89, 97]
    for i in arr:
        tmp = i
        for j in nums:
            if answer % j == 0 and i % j == 0:
                while answer % j == 0 and i % j == 0:
                    i /= j
                    answer /= j
        answer *= tmp
    return answer
```
donghyuk
```py
// code
```
hakim
```py
def gcd(a, b):
    if a % b == 0:
        return b
    return gcd(b, a % b)

def solution(arr):
    if len(arr) == 1:
        return arr[0]
    answer = (arr[0] * arr[1]) / gcd(arr[0], arr[1])
    if len(arr) == 2:
        return answer
    i = 2
    while True:
        answer = (answer * arr[i]) / gcd(answer, arr[i])
        i += 1
        if i == len(arr):
            break
    return answer
```
