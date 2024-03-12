# Determine Data Types

* The "typeof" operator is used to test if a value is a number, string, or function.
* The "Array.isArray" method is used to check if a value is an array.
* null means "no value" or "unknown value". Check that a value is null by using the strict equality operator "x === null".
undefined is used for variables that have not been assigned a value. Test if a value is undefined by using the strict equality operator "x === undefined".

## Null Examples

1. Function to check if a string has consecutive double letters:

```javascript
let hasDoubleLetter = function(str) {
    // Check if the input is a string
    if (typeof str !== 'string') {
        return null;
    }


    for (let i = 0; i < str.length; i++) {
        // check if the current character is the same as the next one
        if (str[i] === str[i + 1]) {
            return true;
        }
    }
    return false;
}
```

2. Function to find the first vowel in a string

```javascript
let firstVowel = function(str) {
    // Define a string of vowels
    let vowels = "aeiou";

    // Iterate through the characters of the input string
    for (let i = 0; i < str.length; i++) {
        // Get the current character
        let char = str[i];

        // Check if the current character is a vowel
        if (vowels.includes(char)) {
            return char;
        }
    }
    // Return null if no vowels are found in the string
    return null;
}
```

3. Function to find the last vowel in a string

```javascript
let lastVowel = function(str) {
    // define a string of vowels
    let vowels - 'aeiou';

    // Iterate through characters in reverse order
    for (let i = str.length - 1; i >= 0; i--) {
        // Get the current character
        let char = str[i];

        // Check if the current character (lowercased) is a vowel
        if (vowels.includes(char.toLowerCase())) {
            return char;
        }
    }
    return null;
}
```
