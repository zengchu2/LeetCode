# 001 Two Sum

## Question
Given an array of integers, <br>
return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, <br>
and you may not use the same element twice.
<br>
## My Solution:
#### Error Chcking
  There is no error checking since there must be a unique solution.

####
  Will simply use a HashMap for stroing integers. We will simply go through each number **i** in array and check wheter
  there is a number **j** in the map such that ***i + j = target***.
  
#### Code-Java
```
    public int[] twoSum(int[] nums, int target) {
        // Since assume there must be one solution.
        HashMap<Integer, Integer> buffer = new HashMap<>();
        buffer.put(nums[0], 0);
        for(int i = 0; i < nums.length; i ++){
            if(buffer.containsKey(target - nums[i])){
                int[] res =  new int[] {i, buffer.get(target - nums[i])};
                return res;
            }
            buffer.put(nums[i], i);
        }
        return new int[] {0, 0};
    }
```
