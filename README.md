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
  
  ### Question 2
  <img width="546" alt="Screenshot 2023-03-25 191046" src="https://user-images.githubusercontent.com/80487497/227749893-36a91223-5656-4dcb-9f90-eb2dfb19ae4b.png">

Solution:
  ```javascript
   var isValid = function(s) {
    const map = {
        ")" : "(",
        "}" : "{",
        "]" : "["
    };
    const arr = [];

    for (i = 0; i < s.length; i++) {

        if (s[i] === "(" || s[i] === "{" || s[i] === "[") {
            arr.push(s[i]);
        }
    
        else { 
            if (map[s[i]] === arr[arr.length - 1]) {
                arr.pop();
            }
            else return false;
        }
    
    }
    return arr.length === 0;
};
  ```
  ##
  
  ### Question 3
  <img width="546" alt="Screenshot 2023-04-01 223723" src="https://user-images.githubusercontent.com/80487497/229331559-25e65a37-75f1-4cb4-9590-111ef348848f.png">

Solution:
  ```javascript
   var maxProfit = function(prices) {
    let min = prices[0]
    let maxProfit = 0
    for (let i = 1; i < prices.length; i++) {
        min = Math.min(min,prices[i])
        maxProfit = Math.max(maxProfit,prices[i] - min)
    }

    return maxProfit;
};
  ```
