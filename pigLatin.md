# Pig Latin

### Problem Description
Pig Latin is a way of altering English Words. The rules are as follows:

- If a word begins with a consonant, take the first consonant or consonant cluster, move it to the end of the word, and add ay to it.

- If a word begins with a vowel, just add way at the end.

Translate the provided string to Pig Latin. Input strings are guaranteed to be English words in all lowercase.

### Problem
```javascript
function translatePigLatin(str) {
  return str;
}

translatePigLatin("consonant");
```

### Solution
<details>
  <summary>
    My answer 🤧
  </summary>
  
  
```javascript
function translatePigLatin(str) {
  if (str.match(/[aeiou]/)) {
    let index = str.indexOf(str.match(/[aeiou]/));
    if (index == 0) 
      return str + "way";
    return str.slice(index) + str.slice(0,index) + "ay";
  }
  return str + "ay";
}

console.log(translatePigLatin("glove"));
```
</details>
