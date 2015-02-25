// challenge 2

function averageMedian(array){
  var length = array.length;

  if (length < 4){
    return "Bad array"
  } else if (length % 2 == 0) {
    // even array
    var index = Math.floor(length/2);
    return calcMedian(array.slice(index-1,index+1));
  } else {
    // odd array
    var index = Math.floor(length/2);
    return calcMedian(array.slice(index-1,index+2));
  }
}

function calcMedian(array){
  var total = 0;
  array.forEach(function(item){
    total += item;
  })
  return total / array.length;
}

// challenge 3

function removeDuplicates(string){
  var hashTable = {};
  var length = string.length;

  stringArray = string.split('');
  stringArray.forEach(function(item, index){
    if (hashTable[item] == null){
      hashTable[item] = [index];
    } else {
      hashTable[item].push(index);
    }
  })

  var keys = Object.keys(hashTable);
  var i = 0;
  keys.forEach(function(item){
    var numLength = hashTable[item].length;
    // console.log(hashTable[item].slice(1, numLength));
    var itemsToRemove = hashTable[item].slice(1, numLength);
    itemsToRemove.forEach(function(item){
      stringArray.splice(item-i, 1);
      i++;
      console.log(item);
    })
  })

  return stringArray.join('');
}
