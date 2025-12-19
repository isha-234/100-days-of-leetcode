```
class Solution:
    def moveZeroes(self, nums: List[int]) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """
        l = 0
        for r in range(len(nums)):
            # when nums is not 0
            if nums[r]: 
                # swap val at l and val at r
                nums[l],nums[r] = nums[r],nums[l]
                l+=1
        return nums
```

        
