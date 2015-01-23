```javascript
// CHALLENGE 1
// Create a bigDiff(array) function that finds the largest number and second largest number of an array, then subtracts the difference.

console.log('>>>>>>>>>>CHALLENGE 1');

// This complexity is O(n^2)
function bigDiff(arr){
  // sort the array from biggest number to smallest number, and then just take the last 2 numbers
  arr.sort(function(a, b){
    return b - a;
  })
  return arr[0] - arr[1];
}

// O() - order of complexity

// for loop - n times
//   for loop - n times
// O(n^2)

// for loop - n times
// for loop - n times
// O(n)

// The complexity is O(n)
function bigDiffHarry(arr){
  var largest_number;
  var second_largest_number;
  var array_length = arr.length;

  if (array_length < 2){
    return "Cannot solve arrays with less than 2 items";
  }

  // assign the first and second item of the array to the largest_number and the second_largest_number
  if (arr[1] > arr[0]){
    // [1,2,99,4]
    second_largest_number = arr[0];
    largest_number = arr[1];
  } else {
    // [2,1,3,565,333,345]
    largest_number = arr[0];
    second_largest_number = arr[1];
  }

  // loop through the array, and constantly replace the largest_number and the second_largest_number if the item at that iteration is larger

  // [3,565,333,345]
  arr.splice(2, array_length).forEach(function(item){
    if (item > largest_number){
      second_largest_number = largest_number;
      largest_number = item;
    } else {
      if (item > second_largest_number && item != largest_number){
        second_largest_number = item;
      }
    }
  })

  return largest_number - second_largest_number;

}

testArray = [3, 6, 9, 12];
bigDiff(testArray);

// CHALLENGE 2
console.log('>>>>>>>>>>CHALLENGE 2');

// CHallenge 3
console.log('>>>>>>>>>>CHALLENGE 3');
```
