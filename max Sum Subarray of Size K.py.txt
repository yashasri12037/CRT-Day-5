class Solution:
    def maxSubarraySum(self, arr, k):
        # code here 
        i=0
        j=0
        win_sum=0
        max_sum=0
        while j<len(arr):
            win_sum+=arr[j]
            if j-i+1!=k:
                j+=1
            elif j-i+1==k:
                max_sum=max(max_sum,win_sum)
                win_sum-=arr[i]
                i+=1
                j+=1
        return max_sum
