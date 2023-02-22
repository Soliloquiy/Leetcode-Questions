# Leetcode Interview Questions

### Question 1
<img width="546" alt="Screenshot 2023-02-22 121311" src="https://user-images.githubusercontent.com/80487497/220734861-4205467a-287b-439c-8d8e-06f5d25068a0.png">


Solution:
  ```javascript
   var twoSum = function(nums, target) {
    const map = {};

    for (let i = 0; i < nums.length; i++) {
        let x = target - nums[i];
        if (x in map) {
            return [map[x], i];
        }
        map[nums[i]] = i;
    }
};
  ```
##
