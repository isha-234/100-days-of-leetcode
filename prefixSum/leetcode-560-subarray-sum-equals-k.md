```
class Solution:
    def subarraySum(self, nums: List[int], k: int) -> int:
        res = 0
        currSum = 0
        prefixSumMap = {0:1}
    
        for num in nums:
            currSum +=num
            diff = currSum - k

            res += prefixSumMap.get(diff,0)
            prefixSumMap[currSum] = 1 + prefixSumMap.get(currSum,0)
        
        return res

        
```
