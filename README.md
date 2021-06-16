# PythonNotes - shortcuts - syntax - cheatsheet

## LIST
if else in a list comprehension

`[x if x>45 else x+5 for x in a]`

```
a=[]    # a==[]
a+=5,   # a==[5]
a+=[3]  # a==[5,3]
```

```
l,*a=eval(dir()[0])
# same as:
l=eval(dir()[0])
a=[]
```

## DICTIONARY
dictionary compehension
```
d = {x[0]: x for x in a}
res = []
for num in arr:
    res += d.get(num, [])
```

vanilla counter
```
for x in arr: myCounter[x]=1+myCounter.get(x,0)
```
## collections
defaultdict
```
from collections import defaultdict
dd = defaultdict(int)
for x in arr:
    dd[x] += 1
```
Counter
```
counts = collections.Counter(arr)
```

```
from collections import Counter
counter = Counter(arr)
```

## DOCUMENTATION
HELP command opens up the documentation from inside the IP SHELL for the functions.
```
help(len)
```
## TRY EXCEPT
Exception Handling

```
try:
  print(x)
except:
  print("An exception occurred")
```

## LRU (least recently used) cache
https://docs.python.org/3/library/functools.html
Decorator to wrap a function with a memoizing callable that saves up to the maxsize most recent calls.
``` @functools.lru_cache(maxsize=128, typed=False)```

If maxsize is set to None, the LRU feature is disabled and the cache can grow without bound.

If typed is set to true, function arguments of different types will be cached separately. For example, f(3) and f(3.0) will be treated as distinct calls with distinct results.
```
import functools as F
@F.lru_cache(maxsize=None)
def f(l,r):

```
```
import functools
@functools.lru_cache(maxsize=4096)
def f(l,r):

```
## itertools
```
itertools.permutations
```
## collections
```
import collections

collections.Counter('asdf')
# Counter({'a': 1, 's': 1, 'd': 1, 'f': 1})
```

## bisect
```
# binary searching
import bisect

def search(nums, target):
    index = bisect.bisect_left(nums, target)
    return index if index < len(nums) and nums[index] == target else -1

print(search([2,4,7,9],9))
```

## ???
find union