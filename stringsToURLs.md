<!-- string to url solutions
regular -->

function stringToURL(string) {
  let arr = string.split(' ');
  let result = '';
  for (let i = 0; i < arr.length; i++) {
    if (i == arr.length - 1) {
      result += arr[i];
    } else {
      result += arr[i] + '%20';
    }
  }
  return result;
}

<!-- recursion -->

<!-- 
given a string
needs to call it self
fencepost edgecase
use split
if arr.length == 1 then its last word
remove word from array
join array -->

const stringToURL = (string) => {
  let arr = string.split(' ');
  let result = arr.slice(0,1);
  if (arr.length == 1) {
    return result;
  }
  arr.shift();
  result += '%20';
  return stringToURL(result + arr.join(' '));
}

