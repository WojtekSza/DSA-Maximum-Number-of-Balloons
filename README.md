# DSA-Maximum-Number-of-Balloons
Given a string text, you want to use the characters of text to form as many instances of the word "balloon" as possible.

You can use each character in text at most once. Return the maximum number of instances that can be formed.
```
Input: text = "loonbalxballpoon"
Output: 2
```
```
from collections import defaultdict
class Solution:
    def maxNumberOfBalloons(self, text: str) -> int:
        counts=defaultdict(int)        
        for s in text: #Time cost of loop O(n)
            counts[s]+=1 #Space cost to store variables O(n)
        counts['l']//=2 # Operation divide cost O(1)
        counts['o']//=2 # Operation divide cost O(1)
        return min(counts['b'],counts['a'],counts['l'],counts['o'],counts['n']) # Min check cost O(1)
    '''
    Total time cost O(n)
    Total space cost O(n)
    '''
```
