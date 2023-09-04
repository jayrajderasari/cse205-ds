class Solution:
    def triangularSum(self, nums: List[int]) -> int:
        def recc(nums):
            newNums = []
            for i in range(0,len(nums)-1):
                temp = (nums[i] + nums[i+1])%10
                newNums.append(temp)
            return newNums
        while len(nums)!=1:
            nums = recc(nums)
        return nums[0]