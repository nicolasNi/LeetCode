Given a collection of numbers that might contain duplicates, return all possible unique permutations.

For example,
`[1,1,2]` have the following unique permutations:
```
[
  [1,1,2],
  [1,2,1],
  [2,1,1]
]
```

[解题思路](http://blog.csdn.net/linhuanmars/article/details/21570835)


```java
public class Solution {
    public List<List<Integer>> permuteUnique(int[] num) {
        ArrayList<List<Integer>> res = new ArrayList<List<Integer>>();  
        if(num==null && num.length==0)  
            return res;  
        Arrays.sort(num);  
        helper(num, new boolean[num.length], new ArrayList<Integer>(), res);  
        return res; 
    }
    
    
    private void helper(int[] num, boolean[] used, ArrayList<Integer> item, List<List<Integer>> res){  
        if(item.size() == num.length)  
        {  
            res.add(new ArrayList<Integer>(item));  
            return;  
        }  
        for(int i=0;i<num.length;i++)  
        {  
            if(i>0 && !used[i-1] && num[i]==num[i-1]) continue;  
            if(!used[i])  
            {  
                used[i] = true;  
                item.add(num[i]);  
                helper(num, used, item, res);  
                item.remove(item.size()-1);  
                used[i] = false;  
            }  
        }  
    }  
}
```

# Python
```python
class Solution:
    def permuteUnique(self, nums: List[int]) -> List[List[int]]:
        res, temp, used =[], [], [False]*len(nums)
        if not nums:
            return res
        nums.sort()
        self.permuteDFS(nums, res, temp, used)
        return res
    
    def permuteDFS(self, nums, res, temp, used):
        if len(temp) == len(nums):
            res.append(copy.copy(temp))
        for i in range(len(nums)):
            if not used[i]:
                if i > 0 and not used[i-1] and nums[i-1] == nums[i]:
                    continue
                used[i] = True
                temp.append(nums[i])
                self.permuteDFS(nums, res, temp, used)
                temp.pop()
                used[i] = False
```
