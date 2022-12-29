# leetcodeRecord
# 001
```
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        result = []
        for i in range(0,len(nums)):
            comple = target-nums[i]

            if comple==nums[i]:
                if comple in nums[i+1:]:
                    j = nums[i+1:].index(comple)+i+1 
                    result.append([i,j])
                else:
                    continue
            else:
                if comple in nums:
                    j = nums.index(comple)
                    result.append([i,j])
                else:
                    continue
            if len(result)>0:
                break
        return result[0]
```
