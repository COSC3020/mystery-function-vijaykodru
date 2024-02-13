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
The above function takes an array 'a' and returns the maximum number in the array
First it checks for the base case where if the array length is 1 it returns the element
if the array length is more than 1 then the function sets a varible named 'foo' to recusivsively call 
the mystery function by slicing the orginally array. What this does is it creates a array with the 
first element removed from the original one. This recurssion happens until the end of the array and 
finally we compare foo with the first element of the array to see which is bigger and finally we return 
the highest numnber.
*/ 
```
