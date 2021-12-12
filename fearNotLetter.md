# Missing letters

### Problem Description
Find the missing letter in the passed letter range and return it.

If all letters are present in the range, return undefined.



### Problem
```javascript
function fearNotLetter(str) {
  return str;
}

fearNotLetter("abce");
```

### Solution
<details>
  <summary>
    My answer :sunglasses:
  </summary>
  
  
```javascript
function fearNotLetter(str) {
  let alphabet = "abcdefghijklmnopqrstuvwxyz";
  let ind = alphabet.indexOf(str[0]);
  alphabet = alphabet.substring(ind);
  for (let i=0; i<str.length; i++) if (str[i] != alphabet[i]) return alphabet[i];
  return undefined;
}

console.log(fearNotLetter("stvwx"));
```
</details>
