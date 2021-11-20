## My Answer
```
class Solution {
    public int[] twoSum(int[] nums, int target) {
        int[] result = null;        
        
        for(int i = 0; i < nums.length - 1; i++) {
            for(int j = i + 1; j < nums.length; j++) {
                if(nums[i] + nums[j] == target) {
                    result = new int[]{i, j};
                }
            }
        }
        
        return result;
    }
}
```
A nested loop was used, so the time complexity is O(n^2).   
URL : [**HERE**](https://leetcode.com/submissions/detail/589961616/)

## Best Answer
```
class Solution {
    public int[] twoSum(int[] nums, int target) {
        Map<Integer, Integer> nums_dict = new HashMap<>();
        for (int i = 0; i < nums.length; i++) {
            int num = nums[i];
            if (nums_dict.containsKey(num)) {
                return new int[] { nums_dict.get(num), i };
            }
            nums_dict.put(target - num, i);
        }
        throw new RuntimeException("No Solution!");
    }
}
```

### Examination of the codes
#### 1. Use a Map collection.
Time complexity for hashmap is O(1) in average cases.
English : https://javabypatel.blogspot.com/2015/10/time-complexity-of-hashmap-get-and-put-operation.html
Korean : https://hee96-story.tistory.com/48#:~:text=%ED%95%B4%EC%8B%9C%20%ED%85%8C%EC%9D%B4%EB%B8%94%EC%9D%98%20%EC%84%B1%EB%8A%A5,%EA%B0%80%20O(1)%EC%9D%B4%EB%8B%A4.

#### 2. No particular data storage just for returning a value
In the best answer, an exception is used instead.

### Knowledge supplement
#### 1. Instantiating an Array in Java
```
int[] arr = new int[20];
arr[0] = 10;
arr[1] = 20;
```
or
```
// In case where the size of the array and variables of array are already known
int[] arr = new int[]{ 1,2,3,4,5,6,7,8,9,10 };
```
https://www.geeksforgeeks.org/arrays-in-java/
#### 2. Hashmap methods
get : https://docs.oracle.com/javase/8/docs/api/java/util/HashMap.html#get-java.lang.Object-    
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Returns the value to which the specified key is mapped, or **null if this map contains no mapping for the key**.
containsKey: https://docs.oracle.com/javase/8/docs/api/java/util/HashMap.html#containsKey-java.lang.Object-
