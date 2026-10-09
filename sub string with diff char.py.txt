class Solution:
    def countGoodSubstrings(self, s: str) -> int:
        i=0
        j=0
        k=3
        c=0
        while j<len(s):
            if j - i + 1 < k:
                j += 1
            elif j-i+1==k:
                if s[i]!=s[i+1] and s[i+1]!=s[i+2] and s[i]!=s[i+2]:
                    c=c+1
                i+=1
                j+=1
        return c
