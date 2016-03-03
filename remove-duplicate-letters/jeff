class Solution(object):
    def removeDuplicateLetters(self, s):
        """
        :type s: str
        :rtype: str
        """
        counter=collections.Counter(s)
        stack=list()
        res=set()
        for c in s:
            counter[c]-=1
            if c in res:
                continue
            while stack and stack[-1]>c and counter[stack[-1]]>0:
                res.remove(stack[-1])
                stack.pop()
            res.add(c)
            stack.append(c)
        return ''.join(stack)
