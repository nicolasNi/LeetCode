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
