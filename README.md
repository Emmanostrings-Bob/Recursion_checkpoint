function isPalindrome(word) {
  const length = word.length;

  // Stop condition: an empty word or a word containing a single character is a palindrome
  if (length === 0 || length === 1) {
    return true;
  }

  const mid = Math.floor(length / 2);

  // Iterate from the start of the word to the middle
  for (let i = 0; i < mid; i++) {
    // Compare the character at index i with the corresponding character from the end of the word
    if (word[i] !== word[length - 1 - i]) {
      // If there is a difference, it's not a palindrome
      return false;
    }
  }

  // If the loop completes without finding differences, it's a palindrome
  return true;
}

// Testing the function
console.log(isPalindrome(""));       // true
console.log(isPalindrome("a"));      // true
console.log(isPalindrome("gag"));    // true
console.log(isPalindrome("kayak"));  // true
console.log(isPalindrome("php"));    // true
console.log(isPalindrome("radar"));  // true
console.log(isPalindrome("hello"));  // false
console.log(isPalindrome("world"));  // false


1.Accept a word as input.
2. Get the length of the word.
3. Check the stop condition:
    . If the word has a length of 0 or 1, return true as it is considered a palindrome.
    . Calculate the midpoint of the word using Math.floor(length / 2).
4. Iterate from the start of the word to the middle using a for loop:
    . Compare the character at index i with the corresponding character from the end of the word (word[length - 1 - i]).
5. If there is a difference, return false as it is not a palindrome.
6. If the loop completes without finding any differences, return true as it is a palindrome.
7. Test the function with different words, including empty words and words with a single character, to verify the palindrome check.


Following these rules: Use of counters and loops
