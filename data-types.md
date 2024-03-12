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

4. A function that returns the smallest number, given an array of numbers.

```javascript
let minValue = function(nums) {
    let min = null;
    for (let i = 0; i < nums.length; i++) {
        let num = nums[i];
        // If the current num is smaller than the current min, replace the min with that number
        if (min === null || num < min) {
            min = num;
        }
    }
    return min;
}
```

5. Return the average value within an array. If the array is empty, the function returns 'null'.

```javascript
let avgVal = function(arr) {
    // Check if the array is empty
    if (arr.length === 0) {
        return null;
    }

    let sum = 0;

    // Iterate through the elements of the array
    for (let i = 0; i < arr.length; i++) {
        let el = arr[i];
        sum += el; // Add each element to the sum
    }

    // Return the average value
    return sum / arr.length;
}
```

6. Find the max value within an array.

```javascript
let maxValue = function(nums) {
    // Initialise a variable to store the max value
    let max = null;

    // Iterate through elements of the array
    for (let i = 0; i < nums.length; i++) {
        let num = nums[i];

        // Check if current element is greater than current max value
        if (max === null || num > max) {
            max = num // Update max value if condition is met
        }
    }
    return max;
}
```

7. Finds the last vowel, returns a word where all the letters after the vowel (including the vowel) are repeated.

```javascript
let reverb = function(word) {
    // Check if the input is a string
    if (typeof word !== 'string') {
        return null;
    }

    // Define string of vowels
    let vowels = 'aeiouAEIOU';

    // Iterate through the characters of the input word in reverse order
    for (let i = word.length - 1; i >= 0; i--) {
        // Check if current character is vowel
        if (vowels.includes(word[i])) {
            // Return concanated word
            return word + word.slice[i];
        }
    }
    return word; // Return original word if no vowels found
}
