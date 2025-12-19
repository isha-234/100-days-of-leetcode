```
class Solution:
    def majorityElement(self, nums: List[int]) -> int:
        n = len(nums)
        numDict = defaultdict(int)

        for num in nums:
            numDict[num] += 1

        for key,val in numDict.items():
            if val > n/2 : 
                return key
        return None
```

