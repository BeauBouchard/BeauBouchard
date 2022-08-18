<h2>Table of Contents</h2>

<details>

  <summary>Table of Contents</summary>

  <ul>
    <li><a href="#table-of-contents">Table of Contents</a></li>
    <li><a href="#common-questions">Common Questions</a>
      <ul>
        <li><a href="#">Find out if two strings are Anagrams</a></li>
        <li><a href="#">First Unique Questions</a></li>
        <li><a href="#">Find out if string is a Palindrome</a></li>
        <li><a href="#">Various String Exercises</a></li>
        <li><a href="#">Various String Exercises</a></li>
      </ul>
    </li>
  </ul>

</details>


Interview Questions which involve improviation of answering a question on the spot, and then coding the question live makes a lot of assumptions around someone's ability and may not be best suited for all interviews. The exercises are interesting and can highlight people's appitude for discovering a solution in real time, but for myself and many others with ADHD or anxiety will often underperform. Most of the same individuals will excell if you give them a study ruberic before a test or explicit instructions and assuptions for a take home assement; however doing the same thing blind and improvied can be a disasterous challange that requires more from their ability to not have stage shock than problem solving. 
I have spent time testing out various ways to solve puzzles find them fun and I expect most of these to appear at least once in an interview process for someone some day, its worth to have more discussion around using these resources and what they are trying to assertain from a canidate. I absolutly love puzzles but I can't even do a handshake correctly under pressure, you're not going to get the best live coding experience from me, but whiteboarding and giving me an exercise to work on and later review are my favorite. 

I wanted to demonstrate some of the nuances in these questions to both practice them as a learning exercise but also to demonstrate and articulate some of these more interesting subtle sub-questions of these exercises. 

If you are a hiring manager and you have a decision to give a live coding exercise to an itnerviewee I always recommend to white board or even better offer the assignment as a take home and review the code later in a very relivant peer review setting. 

## Common Questions

### Find out if two strings are anagrams.


#### Example question format
An Anagram is a word, phrase, or name formed by rearranging the letters of another, such as cinema, formed from iceman.
Finish the following function to return true if the words are anagrams, or false if they are not anagrams

```js
/** 
 * @param {string} wordOne - the first word to check against
 * @param {string} wordTwo - the second word to check against first word
 * @return {boolean} - return true if the words are anagrams of eachother or false if they are not anagrams
 **/
 function isAnagram(wordOne,wordTwo) {
 
 }

// Part 1
// This statement should be false
console.log(isAnagram("cat","dog"));
// This statement should be true
console.log(isAnagram("cinema","iceman"));


// Part 2 
// This statement should validate TRUE
console.log(isAnagram("YDA SRMADE","daydream"));
```

#### Example Solution and Explaination

###  First Unique Questions

This question comes in a few different formats, but mostly its about eliminiating duplicates and finding uniques. 

I can be phrased as `Finding the first unique character in a string` or performing search in arrays, or other datastructures. 

#### Example question format
Given a string s, find the first non-repeating character in it and return its index. If it does not exist, return -1.
```js
/** 
 * @param {string} word - the word to check if it has unique characters
 * @return {number} - the position where the first unique character exists
 **/
 function firstUniqChar(word) {
 
 }
 
// Part 1
// This statement should be 0
// console.log(firstUniqChar("code"));
// This statement should be 2
// console.log(firstUniqChar("bearsarebeautiful"));
// This statement should be -1
// console.log(firstUniqChar("aabb"));
```


#### Example Solution and Explaination


### Find out if a string is a palindrome

A Palindrome is a word, phrase, or sequence that reads the same backward as forward, e.g., `madam` or `nurses run`.
A string is said to be a Palindrome if the reverse of teh string is same as itself. 

#### Example question format in Javascript 

Finish the following function to return true if the word is a palindrome (same front to back) or false if it is not.

```js
/** 
 * @param {string} word - the word to check if it is a Palindrome
 * @return {boolean} - return true if the word is a palindrome (same front to back) or false if it not a palindrome.
 **/
 function isPalindrome(word) {
 
 }

// Part 1
// This statement should be false
// console.log(isPalindrome("cat"));
// this statement should be true
// console.log(isPalindrome("madam"));
// This statement should be true
// console.log(isPalindrome(`nurses run`));

// Part 2
// Instead of returning true, have it return how many non-empty strings are palindromes. A substring is any continuous sequence of characters in the string.  Two sub strings are different if they occur at different positions in `word`.  
/** 
 * @param {string} word - the word to check if it is a Palindrome
 * @return {number} - return how many non-empty strings are palindromes
 **/
 function howManyPalindromes(word) {
 
 }
 

// console.log(howManyPalindromes(`abaabbbba`));
```

#### Example Solution in Javascript 

```js

/** 
 * @param {string} word - the word to check if it is a Palindrome
 * @return {boolean} - return true if the word is a palindrome (same front to back) or false if it not a palindrome.
 **/
 function isPalindrome(word) {
  // using recusion
  const length = word.length;
  if (length <= 1){
    return true;
  } else if (word.charAt(0) !== word.slice(-1)) {
    return false;
  } else {
    return isPalindrome(word.substring(1,length-1));
  }
}

// Part 1
// This statement should be false
console.log(isPalindrome("cat"));
// this statement should be true
console.log(isPalindrome("madam"));
// This statement should be true
console.log(isPalindrome(`nurses run`));


// Part 2
// Instead of returning true, have it return how many non-empty strings are palindromes. A substring is any continuous sequence of characters in the string.  Two sub strings are different if they occur at different positions in `word`.  
/** 
 * @param {string} str - the string to check if it is a Palindrome
 * @return {number} - return how many non-empty strings are palindromes
 **/
 function howManyPalindromes(str) {
    // The trick for part two is counting the loop progression using a variable 
    let count = 0;
    const length = str.length;
    let subString;

    for (let i = 1; i < length; i++) {
      for(let j = 0; j < length - i; j++) {
        subString = str.substring(j, j+i+1);
        // the trick to part 2 is checking the split / reverse
        if(subString === subString.split('').reverse().join('')) {
            count += 1;
        }
      }
    }
    return count;
 }
 
 // Part 3 could be unique palindromes

```



### The Prime number Questions

There are many exercises that involve prime numbers, most of them involve finding if a number is prime or not, or generating prime numbers from 0 to N. 

There are different complexities with space (memory) and time where you are able to have a more optimized method. 

Common questions you may not know and the interviewer may need to provide: 

* Is 1 a prime number?  
 * No
* What is a Prime Number? 
 * A prime number is a whole number greater than 1 with only two factors – themselves and 1.

#### Example question format in Javascript 

```js
// Make the following function detect if the number passed into it "N" is a prime number
function isPrime (num) {

}
```

#### Example Solution in Javascript 

You will want to be creating a loop which itterates between all possible values from Num to zero. 

My own solution was very ugly when i did this exercise myself without any research. 



```js
// Make the following function detect if the number passed into it "N" is a prime number
// A Prime number is a number which is divisible only with itself and 1. 
/**
 * @param {Number} num - the number to detect if it is a prime number
 * @return {Boolean} - returns true if the number is a prime number, returns false if not
 **/
function isPrime (num) {
  // if number is 1, or less than 1 we can return false. 1 is not a prime number
  // I toy around and make a few solutions for this which would wastes time 
  // and be a distraction i would try to avoid if I had a delivery/timelimit to hit :P 
  // return num !== 1 && num !== 0
  // if((number % 2 === 0 && number !== 2) || number <= 1) {
  //  return false;
  //}
  // I chose the most readable one, as its more important to understand the code, optimization of efficiency is a secondary luxury to the primary of accuracy. 
  // if number is 1, or less than 1 we can return false. 1 is not a prime number
  if (num <= 1) {
    return false;
  }
  // 2 and 3 are prime we can skip calcuating them
  if (num === 2 || num === 3) {
    return true;
  }

  // mod squareroot is zero means non-prime
  if (num % Math.sqrt(num) === 0) {
    return false;
  }
}

// testing
for(let i=-2; i <= 35; i++) { 
  console.log(`${i} is${isPrime(i) ? '' : ' not'} prime`);
}

```



I researched [a better solution](https://stackoverflow.com/a/40200710/1205637) which included a lot of nuance and understanding which I think is worth crediting. From that I think this solution was probably one that would be more optimized and accepted as one of the better ones. 

```js
// Make the following function detect if the number passed into it "N" is a prime number
// A Prime number is a number which is divisible only with itself and 1. 
/**
 * Square Root For Loop Optimized Solution
 * Time complexity: O(sqrt(n))
 * Space complexity: O(1)
 * @param {Number} num - the number to detect if it is a prime number
 * @return {Boolean} - returns true if the number is a prime number, returns false if not
 **/
function isPrime (num) {
  for(let i = 2, s = Math.sqrt(num); i <= s; i++) {
    if(num % i === 0) {
      return false; 
    }
  }
  return num > 1; // return num !== 1 && num !== 0; removed to use condition
}

// testing
for(let i=-2; i <= 35; i++) { 
  console.log(`${i} is${isPrime(i) ? '' : ' not'} prime`);
}
```






