```
class Solution:
    def maxProfit(self, prices: List[int]) -> int:
        # minimum = float('inf')
        # maximum = 0

        # for i in range(len(prices)):
        #     minimum = min(minimum, prices[i])
        #     maximum = max(maximum, prices[i] - minimum)
        
        # return maximum

        l,r = 0,1
        maxProfit = 0

        while r < len(prices):
            if prices[l]<prices[r]:
                maxProfit = max(maxProfit, prices[r] - prices[l])
            else:
                l = r
            r +=1
        return maxProfit


```
