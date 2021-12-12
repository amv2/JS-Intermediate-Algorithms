# DNA Pairing

### Problem Description
The DNA strand is missing the pairing element. Take each character, get its pair, and return the results as a 2d array.

Base pairs are a pair of AT and CG. Match the missing element to the provided character.

Return the provided character as the first element in each array.

For example, for the input GCG, return [["G", "C"], ["C","G"], ["G", "C"]]

The character and its pair are paired up in an array, and all the arrays are grouped into one encapsulating array.



### Problem
```javascript
function pairElement(str) {
  return str;
}

pairElement("GCG");
```

### Solution
<details>
  <summary>
    My answer 
  </summary>
  
  
```javascript
function pairElement(str) {
  str = str.split('')
  for(let i=0; i<str.length; i++) {
    str[i] = str.slice(i,i+1)
    if (str[i].includes("A")) str[i].push("T")
    else if (str[i].includes("C")) str[i].push("G")
    else if (str[i].includes("G")) str[i].push("C")
    else if (str[i].includes("T")) str[i].push("A")
  }
  return str;
}

console.log(pairElement("CTCTA"));
```
</details>
