# Algorithm 💹

## 🎲  규칙

- 매일 아침 알고리즘 문제를 푼다!
- 풀이한 문제의 폴더안에 README.md 파일에 자신의 풀이를 넣는다.(방법은 밑에)

## 풀이한 문제 작성 방법

- 문제에 해당하는 폴더안에 README.md로 가서 아래 코드를 추가한다.
- 밑에 코드를 복사 붙여넣고 이름을 수정하고 코드 블럭에 자신이 풀이한 코드를 넣으면 된다.
```html
## 아래 코드는 md 파일에 토글 넣는 방법입니다.
<details>
<summary>이름</summary>
<div markdown=“1”>

 코드블럭 
  
</div>
</details>
```

- 만약 문제 폴더가 없거나 추가로 넣고 싶으면 홈에서 Add file -> Create New File 을 누른다.
- 파일 명에 문제이름/README.md 를 작성하면 폴더를 생성하면서 README.md를 수정할 수 있다.
- README.md를 수정할 때 맨 위에 문제 링크를 넣어주고 자신의 위 방법으로 자신의 코드를 넣어준다.
- 밑에 폴더 링크도 추가해주면 감사하겠습니다.^^
- 링크 추가 방법: `[폴더이름](링크주소)`

## 🔗 코딩테스트
- **[프로그래머스](https://programmers.co.kr/learn/challenges)**
- **[백준](https://www.acmicpc.net/)**

## 💬 문제 풀이
- [모의고사](https://github.com/knotted-developers/Algorithm/tree/main/모의고사)
- [신규아이디추천](https://github.com/knotted-developers/Algorithm/tree/main/신규아이디추천)
- [비밀지도](https://github.com/knotted-developers/Algorithm/tree/main/비밀지도)
- [거리두기 확인하기](https://github.com/knotted-developers/Algorithm/tree/main/거리두기%20확인하기)
- [문자열 압축](https://github.com/knotted-developers/Algorithm/tree/main/문자열%20압축)
- [다트던지기](https://github.com/knotted-developers/Algorithm/blob/main/%EB%8B%A4%ED%8A%B8%EB%8D%98%EC%A7%80%EA%B8%B0/README.md)
- [다음 큰 숫자](https://github.com/knotted-developers/Algorithm/tree/main/%EB%8B%A4%EC%9D%8C%20%ED%81%B0%20%EC%88%AB%EC%9E%90)
- [타겟 넘버](https://github.com/knotted-developers/Algorithm/blob/main/%ED%83%80%EA%B2%9F%20%EB%84%98%EB%B2%84/README.md)
- [네트워크](https://github.com/knotted-developers/Algorithm/tree/main/%EB%84%A4%ED%81%AC%EC%9B%8C%ED%81%AC)
- [그리디 알고리즘](https://github.com/knotted-developers/Algorithm/tree/main/%EA%B7%B8%EB%A6%AC%EB%94%94%20%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98)
- [여행경로](https://github.com/knotted-developers/Algorithm/tree/main/%EC%97%AC%ED%96%89%EA%B2%BD%EB%A1%9C)
- [소수 찾기](https://github.com/knotted-developers/Algorithm/tree/main/%EC%86%8C%EC%88%98%20%EC%B0%BE%EA%B8%B0)
- [DFS](https://github.com/knotted-developers/Algorithm/tree/main/DFS)

# 코딩테스트 때 쓰이는 것들 모음

## heap - 힙 ✔️
```python
import heapq # 기본은 min-heap, max-heap 사용시 -값 넣기

lst = [1, 2, 3]
heapq.heapify(lst)
# 빈 배열은 push시 자동으로 힙으로 됨
empty = []
```
#### 💡 삽입 / 제거 / 조회
```python
heapq.heappop(my_list)
heapq.heappush(my_list, -1)
my_list[0]
```
<hr>

## queue - 큐 ✔️
```python
from collections import deque
que = deque([1, 2, 3])
```

#### 💡 원소 중간 삽입
```python
que.insert(i, num)
```
#### 💡 삽입 / 제거 / 조회
```python
que.append(item)
que.popleft()
que[0]
```
<hr>

## counter ✔️
```python
import collections
my_list = ["a", "a", "b", "b", "c"]
collections.Counter(my_list)

# Counter({'a': 2, 'b': 2, 'c': 1})
```

<hr>

## itertools ✔️
```python
import itertools
from itertools import permutations
from itertools import combinations
from itertools import product
from itertools import chain
```
<hr>

### 💡 permutations - 순열
```python
permutations(range(1, 10), 3)
permutations(lst)
```
### 💡 combinations - 조합
```python
combinations('ABC', 2)
```
### 💡 product - 중복순열 
```python
product(range(1,n1+1), range(1,n2+1), range(1,n3+1))

or_not = [(0, 500), (0, 1500)]
list(product(*or_not))

#[(0,0), (0,1500), (500,0), (500,1500)]
```
### 💡 chain - flatten(2차배열 ->1차배열)
```python
itertools.chain(*board)
chain(*board)
```

<hr>

## dictionary - 해시 ✔️
#### 💡 get
```python
my_dict['total']
my_dict.get('total', 0)
```
#### 💡 제거 - pop : 키가 없는 경우 default 리턴
```python
my_dict.pop('홍길동', 180)
```
#### 💡 탐색
```python
dict.items()
dict.keys()
dict.values()
```

#### 💡 그래프 셋팅 :  get 사용
```python
nodes = {}
for v1, v2 in edge:
    nodes[v1] = nodes.get(v1, []) + [v2]
    nodes[v2] = nodes.get(v2, []) + [v1]
```

#### 💡 그래프 셋팅 with dist :  get 사용
```python
nodes = {}
for v1, v2, d in road:
    nodes[v1] = nodes.get(v1, []) + [(v2, d)]
    nodes[v2] = nodes.get(v2, []) + [(v1, d)]
```

#### 💡 그래프 셋팅 거리 초기화
```python
dist = { i:float('inf') if i != 1 else 0 for i in range(1, N+1) }
```
<hr>

## defaultdict ✔️
```python
from collections import defaultdict

dict1 = defaultdict(set)
dict2 = defaultdict(list)
dict3 = defaultdict(int) -> 0으로 셋팅
```

#### 💡 그래프 셋팅 :  defaultdict 사용
```python
from collections import defaultdict
nodes = defaultdict(list)
for v1, v2 in edge:
    nodes[v1].append(v2)
    nodes[v2].append(v1)
```
<hr>

## set - 셋 ✔️
#### 💡 삽입 / 제거
```python
my_set.add(3)
my_set.remove(3)
```
#### 💡 include
```python
if 3 in my_set:
	print('3 있음')
if 3 not in my_set:
	print('3 없음')
```
#### 💡 합집합, 교집합, 차집합
```python
set1 | set2
set1.update(set2)

set1 - set2

set1 & set2
```
<hr>

## bisect ✔️
```python
from bisect import bisect_left, bisect_right
```
#### 💡 최소값 바로 왼쪽 (최소값 들어갈 index)
```python
bisect_left(lst, start)
```
#### 💡 최대값 바로 오른쪽 (최대값 들어갈 index)
```python
bisect_right(lst, end)
```
#### 💡 count_by_lange
```python
def count_by_lange(lst, start, end):
    return bisect_right(lst, end) - bisect_left(lst, start)
```
<hr>

## DELTA - 방향 ✔️
```python
DELTAS = [(0, 1), (0, -1), (-1, 0), (1, 0)] # 오른쪽 왼쪽 위 아래
DELTAS = [(-1, 0, UP), (1, 0, DOWN), (0, 1, RIGHT), (0, -1, LEFT)]
DELTAS = {'U':(0, 1), 'D':(0, -1), 'L':(-1, 0), 'R':(1, 0)}

DELTAS = {'U': (-1, -1), 'D': (1, 0), 'R': (0, 1)}
NEXT = {'U': 'D', 'D': 'R', 'R': 'U'}
```
<hr>

## visitable - 탐색 범위 확인 ✔️
```python
def visitable(y, x, m, n):
    return 0 <= y < m and 0 <= x < n
```
<hr>

## 소수 ✔️
```python
N, primes = end_num, set()
prime_check = [False, False] + [True]*(N-1)

for i in range(2, N+1):
    if prime_check[i]:
        primes.add(i)
        prime_check[i*2::i] = [False] * len(prime_check[i*2::i])
```
<hr>

## 최소공배수 / 최대공약수 ✔️
#### 💡 최대공약수
```python
from fractions import gcd
gcd(6,8) # 2
```
#### 💡 최소공배수
```python
def lcm(a,b):
    return  a * b // gcd(a, b)
```
<hr>

## 곱으로 나타내기 ✔️
```python
[(number//i, i) for i in range(1, int(number**.5)+1) if number % i == 0]
# number = 24 -> 곱해서 24가되는 경우
[(24, 1), (12, 2), (8, 3), (6, 4)]
```
<hr>

## 이분탐색 ✔️
#### 💡 최소값
```python
def impossible(n, middle, times):
    return sum([middle // x for x in times]) < n

def solution(n, times):
    left, right = 1, max(times)*n
    while left < right:
        middle = (left + right) // 2
        if impossible(n, middle, times): 
            left = middle + 1
        else: 
            right = middle
    return left
```
#### 💡 최대값
```python
def is_poss(middle, budgets, M):
    return M >= sum([min(middle, budget) for budget in budgets])

def solution(budgets, M):
    left, right = 1, max(budgets)
    while left < right:
        middle = (left + right + 1) // 2 
        if is_poss(middle, budgets, M):
            left = middle
        else:
            right = middle - 1
    return right
```
<hr>

## sort ✔️
#### 💡 sort
```python
lst.sort()
dist.sort(reverse=True)
lst.sort(key= lambda x : (x*4)[:4], reverse=True)
```
#### 💡 sorted
```python
sorted(lst)
sorted(lst, reverse=True)
sorted(answer, key = lambda x : (x[0], -x[1], x[2]))
```
<hr>

## count ✔️
#### 💡 요소 개수 세기
```python
lst.count(0)
[*row, *col, *diag].count(n)
```
#### 💡 filter count
```python
filter = [item for item in items if 조건식 ]
len(filter)
```
<hr>

## 2차배열 ✔️
#### 💡 초기화 m * n 행렬
```python
board = [[0] * n for i in range(m)]
```
#### 💡 행열 뒤집기 (n*m)
```python
reversed = list(map(list,zip(*board)))
```
#### 💡 90도 회전
```python
def rotate90(arr):
    return list(zip(*arr[::-1]))
```
<hr>

## string ✔️
#### 💡 글자 replace
```python
query.replace('?','a')
```
#### 💡 기준으로 쪼개기
```python
s.split("},{")
```
#### 💡 join
```python
number = int(''.join(x))
```
#### 💡 string 갯수 단위로 쪼개기
```python
splited = [s[i:i+size] for i in range(0, LENGTH, size)]
# size = 3 : aabbaccc -> ['aab', 'bac', 'cc']
```
<hr>

## 정규식
```python
import re
```
#### 💡 찾기
```python
re.search("^"+pre+".+",number)
re.findall(query, word)
lst = re.findall('\d+',s)
# ['2', '2', '1', '3', '4']
re.compile("(\D)")
```
<hr>

## 원형 선형으로 ✔️
```python
weak_point = weak + [w+n for w in weak]
```
<hr>

## math ✔️
```python
import math
```
#### 💡 ceil
```python
math.ceil(num / div)
```
#### 💡 factorial
```python
math.factorial(3)
```
