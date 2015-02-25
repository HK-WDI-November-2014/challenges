function removeDuplicates(string){
  // we could have used a nested for loop to find duplicates, but the complexity would be O(n^2), but Harry wants O(n)

  // If you have one million users, and you want to see how many people have the same birthday, and I want to find the number of people who have the same birthday on a specific date on demand, what do you do?

  // hashTable = {
  //   "Jan 1st 1950": 0,
  //   "Jan 2nd 1950": 0,
  //   "Jan 3rd 1950": 0,
  //   ...
  // }

  var hashTable = {};
  var length = string.length;

  // "abc" => ['a','b','c']
  var stringArray = string.split('');

  // var string = "aabbc"
 // var hashTable = {
  //   "a": [0,1],
  //   "b": [2,3],
  //   "c": [4]
  // }
  stringArray.forEach(function (item, index) {
    if (hashTable[item] == null){
      hashTable[item] = [index]
    } else {
      hashTable[item].push(index);
    }
  });

  // ['a','b','c']
  var keys = Object.keys(hashTable);
  var i = 0;
  keys.forEach(function (item) {
    // hashTable[item] == [0,1,2,3,4] if item == 'a'
    // 2
    var numOccurrence = hashTable[item].length;

    // [1,2,3,4]
    var itemsToRemove = hashTable[item].slice(1, numOccurrence);
    itemsToRemove.forEach(function (index) {
      stringArray.splice(index-i, 1);
      i++;
    });
  });

  return stringArray.join('');

}

function removeDuplicates2(string){
  var hashTable = {};
  var length = string.length;

  var stringArray = string.split('');
  var newArray = [];

  stringArray.forEach(function (item) {
    if (hashTable[item] == null){
      hashTable[item] = 1;
      newArray.push(item);
    } else {
      hashTable[item]++;
    }
  });

  return newArray.join('');
}
