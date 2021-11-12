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