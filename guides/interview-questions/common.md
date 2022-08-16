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
      </ul>
    </li>
  </ul>

</details>


Interview Questions which involve some coding are a silly thing to do in person, the exercises are interesting and can highlight people's abilities discovering a solution in real time. But for myself and many others I get anxious and underperform and find string based questions particularly challanging while observed due to dyslexia. 
I have spent time testing out various ways to solve puzzles find them fun and I expect most of these to appear at least once in an interview process for someone some day, its worth to have more discussion aroudn using these resources and what they are trying to assertain from a canidate. 

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

```

