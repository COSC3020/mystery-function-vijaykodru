[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/GDPVb20V)
# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    if(a.length == 1) return a[0];
    var foo = mystery(a.slice(1, a.length))
    if(foo > a[0]) return foo;
    else return a[0];
}

/*
The above function takes an array 'a' and returns the maximum number in the array or the maximum element (String).
First, it checks for the base case where if the array length is 1 it returns the element
if the array length is more than 1 then the function sets a variable named 'foo' to recursively call 
the mystery function by slicing the original array. What this does is it creates an array with the 
first element removed from the original one. This recursion happens until the end of the array and 
finally, we compare foo with the first element of the array to see which is bigger. Javascript compares strings in lexicographical order.
The elements are compared character by character accordingly and the greatest one will be returned.
For example, if we compare ABC and ABE the maximum will be ABE. Likewise, if we compare A5B and A6B the maximum will be A6B.
So finally the function returns the highest element.

Reference: https://javascript.info/comparison#:~:text=String%20comparison,compared%20letter%2Dby%2Dletter.
*/
