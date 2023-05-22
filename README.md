function isPalindrome(word) {
  word = word.toLowerCase(); // Convert word to lowercase for case-insensitive comparison
  let left = 0; // Initialize left pointer
  let right = word.length - 1; // Initialize right pointer

  while (left < right) { // Continue until left pointer crosses right pointer
    if (word[left] !== word[right]) { // If characters at left and right positions are not equal
      return false; // Word is not a palindrome, return false
    }
    left++; // Move left pointer to the right
    right--; // Move right pointer to the left
  }

  return true; // All characters matched, word is a palindrome, return true
}

// Test the function
const word1 = "gag";
const word2 = "kayak";
const word3 = "php";
const word4 = "radar";
const word5 = "hello";

console.log(isPalindrome(word1)); // true: "gag" is a palindrome
console.log(isPalindrome(word2)); // true: "kayak" is a palindrome
console.log(isPalindrome(word3)); // true: "php" is a palindrome
console.log(isPalindrome(word4)); // true: "radar" is a palindrome
console.log(isPalindrome(word5)); // false: "hello" is not a palindrome
