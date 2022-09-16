class Solution:
    def findOriginalArray(self, changed: List[int]) -> List[int]:
        ctr = Counter(changed)
        res = []
		
        for num in sorted(ctr):
            if num == 0: # Special case
                if ctr[num] % 2 == 0:
                    res.extend([0]*(ctr[num] // 2))
                else:
                    return []
            elif ctr[num] != 0:
                if num*2 not in ctr or ctr[num*2] < ctr[num]:
                    return []
                ctr[num*2] -= ctr[num]
                res.extend([num]*ctr[num])
        return res
