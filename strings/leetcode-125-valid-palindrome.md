```
class Solution:
    def preprocess(self,s: str) -> str:
        res = ""
        for char in s:
            if char.isalnum():
                res += char.lower()
        return res
    def isPalindrome(self, s: str) -> bool:
        s = self.preprocess(s)
        left = 0
        right = len(s) - 1

        while left < right:
            if s[left] != s[right]:
                return False
            left += 1
            right -= 1
        return True
        
```
