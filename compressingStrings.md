<!-- Compressing Strings -->

<!-- Normal Solution -->

<!-- 
given a string
split into arr
set counter
add to result-->

function compressingStrings(string) {
  let arr = string.split('');
  let result = '';
  let repeatedCount = 1;
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] != arr[i + 1]) {
      if (repeatedCount != 1) {
        result += repeatedCount;
      }
      result += arr[i];
      repeatedCount = 1;
    } else {
      repeatedCount++;
    }
  }
  return result;
}