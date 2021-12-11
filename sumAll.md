# Sum All Numbers in a Range

### Problem Description
We'll pass you an array of two numbers. Return the sum of those two numbers plus the sum of all the numbers between them. The lowest number will not always come first.

For example, sumAll([4,1]) should return 10 because sum of all the numbers between 1 and 4 (both inclusive) is 10.

### Problem
```javascript
function sumAll(arr) {
  return 1;
}

sumAll([1, 4]);
```

### Solution
<details>
  <summary>
    My answer :hand_over_mouth:
  </summary>
  
  
```javascript
function sumAll(arr) {
  let start, end, sum = 0;
  if (arr[0] < arr[1]) {
    start = arr[0];
    end = arr[1];
  } else {
    start = arr[1];
    end = arr[0];
  }
  for (let i=start; i<=end; i++) {
    sum += i;
  }
  return sum;
}

sumAll([1, 4]);
```
</details>
