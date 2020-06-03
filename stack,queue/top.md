## 1. 처음 시도

```python
def solution(heights):
    answer = []
    i = 0;
    while (i < len(heights)):
        j = i - 1
        answer.append(0)
        while (j >= 0):
            if heights[j] > heights[i]:
                answer[i] = j + 1
                break
            j -= 1
        i += 1

    return answer
```



## 2. 두번째 시도(다른답 참고 range 사용)

```python
def solution(heights):
    answer = [0] * len(heights)
    for i in range(len(heights)):
        for j in range(i-1,-1,-1):
            
            if heights[j] > heights[i]:
                answer[i] = j + 1
                break
    return answer
```

