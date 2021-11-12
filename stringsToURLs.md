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