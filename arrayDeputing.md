<!-- Array Deduping solutions -->

<!-- Normal Solution -->

<!-- 
given an array
want to remove duplicates
nested loop?
j is i + 1 for inside loop
splice? -->

function arrayDeduping (array) {
  let arr = array;
  for (let i = 0; i < arr.length; i++) {
    for (let j = i + 1; j < arr.length; j++) {
      if (arr[j] == arr[i]) {
        arr.splice(j, 1);
      }
    }
  }
  return arr;
}

<!-- Recursion Solution -->

<!-- 
given an array
want to remove duplicates
needs to call it self
-->

const arrayDedupe = (array) => {
  helper(array, 0)
}

const arrayDeduping = (array, index) => {
  let result = [];
  if (array.length == 0) {
    return result;
  }
  for (let i = 1; i < array.length; i++) {
    if (array[i] != array[0]) {
      result.push(array[i]);
    }
  }
  return arrayDeduping(result);
}