// Challenge 1: Palindrome 
// Using JavaScript, write a function to return the string "true" if str, where str is a string, is a palindrome.
// Example 1: str = "racecar"
// Expected result: "true"
// Example 2: str = "chipmunk"
// Expected result: "false"

function isPalindrome(string){
  var length = string.length - 1;
  stringArray = string.split('');

  for(var i = 0; i <= length / 2; i++){
    console.log(stringArray[i], stringArray[length-i]);

    if (stringArray[i] != stringArray[length-i]){
      return false;
    }
  };

  stringArray.forEach(function(item){
    // Doesn't work
    return false
  })

  return true;
}

// Challenge 4:
// Create a countClumps(array) function: Returns the number of times 2 or more of the same number appear sequentially.
// Example:
// [2, 1, 1, 1, 1, 3, 3, 3, 1] => 2
// [9, 3, 3, 4, 4, 4, 6, 7, 7, 7] => 3

function countClumps(array){
  var totalCount = 0;
  var sequentialCount = 0;
  var prevItem = null;
  var valid = false;

  array.forEach(function(item){
    if (prevItem == null){
      prevItem = item;
    } else if (item == prevItem){
      sequentialCount++;
      if (sequentialCount >= 1){
        valid = true;
      }
    } else {
      if (valid == true){
        totalCount++;
      }
    }

    prevItem = item;
  })

  return totalCount;
}
