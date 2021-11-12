<!-- Array Sorting -->

<!-- Normal Solution -->

<!-- 
given an array 
sort array 
cant use sort method 
are we only given an array of numbers?
if not in what way do we sort other things?
nested loop
if statement to compare current and iterated numbers -->

function sortArray(arr) {
  let array = arr;
  for (let j = 0; j < array.length; j++) {
    for (let i = 0; i < array.length; i++) {
      if (array[i] > array[i + 1]) {
        let placeholder = array[i];
        array[i] = array[i + 1];
        array[i + 1] = placeholder;
      }
    }
  }
  return array;
}