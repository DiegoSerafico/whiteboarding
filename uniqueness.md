<!-- Checking for Uniqueness -->

<!-- Normal Solution -->

<!-- 
check for uniqueness (assuming this means no repeating characters)
returns a boolean
cant use array or its methods
given a string -->

function uniqueness(string) {
  let isUnique = true;
  for (var i = 0; i < string.length - 1; i++) {
    if (string.charAt(i) === string.charAt(i + 1)) {
      isUnique = !isUnique;
      break;
    }
  }
  return isUnique;
}