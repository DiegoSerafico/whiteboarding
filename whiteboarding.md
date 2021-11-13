<!-- Question 3: Compressing Strings -->

<!-- 
algorith that take a string with repeated characters
compress them to show how many times they are compressed
all characters
-->

 <!-- 
 Input: 'aaabccdddda'
 Output: '3ab2c4da'
  -->


  <!-- 
just strings upper and lower case

given a string 
upper and lower case are different

split the string
create and empty result strings
start counter
iterate through the split string
add the number and repeated letter that corresponds
no number if letter is on its own
reset counter
   -->

const compressedString = (string) => {
  let arr = string.split('');      
  let result = '';
  let counter = 1;
  for (let i = 0; i < arr.length; i+=) {
    if (arr[i] != arr[i + 1]) {
      if (counter != 1) {
        result += counter;
      }
      result += arr[i];
      counter = 1;
    } else {
      counter++;
    }
  }
  return result;
}

<!-- input 'aaabccdddda'  [a,a,a,b,c,c,d,d,d,d,a] -->