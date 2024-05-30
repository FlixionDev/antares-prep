### JavaScript Questions

### Theory Questions
1. What is the difference between `var`, `let`, and `const` in JavaScript?
Ans:-`var` is Function-scoped or globally-scoped.  `let`, and `const` is Block-scoped. `var` can be redeclared and updated where `let` cannot be redeclared within the same scope but can be updated. `const` cannot be redeclared or updated.

2. Explain the concept of closures in JavaScript with an example.
Ans:-Closure is a function is bind together to its lexical environment or Function along with the lexical scope form a closure. ex. Closures are an ability of a function to remember the variables and functions that are declared in its outer scope. Suppose function a and function b and function a is parent of function b. There variable num=10 declared in function A and if console log in function to variable num it show show 10 in cconsole this happen due closure.

3. What are promises in JavaScript and how do they work?
Ans:-Promises are objects representing the eventual completion or failure of an asynchronous operation. They have three states: pending, fulfilled, and rejected.

4. What is the purpose of the `this` keyword in JavaScript? Provide an example.
Ans:-The `this` keyword refers to the object that is executing the current function. It’s dynamic and determined by how a function is called.

5. What are arrow functions and how do they differ from regular functions?
Ans:-Arrow functions provide a shorter syntax for writing functions. Normal function declaration is function A(){} and the arrow fuction declaration is const A=()=>{} and also they do not have their own `this`.

6. Describe how JavaScript handles asynchronous operations.
Ans:- JavaScript handles asynchronous operations using callbacks, promises, and async/await. 

7. What is the event loop in JavaScript? How does it work?
Ans:-The event loop is a mechanism that JavaScript uses to handle asynchronous operations. It continuously checks the call stack and the task queue, and if the call stack is empty, it pushes the first task from the queue to the call stack.

8. Explain the concept of hoisting in JavaScript with examples.
Ans:-Hoisting is phinomina in javascript where you can access the variable before its initialize it. Because when execution context is created in two phase first is memory creation phase and code execustion phase. In first phase variable and function store in key-value pair for variable is variable name is the key and value should be undefined and for function it store value as whole code.
only a variable with `var` declaration is hoisted not let and const. 

9. What is the difference between `==` and `===` in JavaScript?
Ans:- Both are comparison operators. The difference between both the operators is that == is used to compare values whereas, === is used to compare both values and types.


### Code Implementation Questions

1. Write a function to reverse a string in JavaScript.
Ans:-let str = "hello";
function reverseString(str) {
    let rev = "";
    for (let i = str.length - 1; i >= 0; i--) {
        rev += str[i];
    }
    return rev;
}
console.log(reverseString(str));   //output:- olleh

2. Create a function that removes duplicates from an array.
Ans:-
let arr=[1,2,3,4,2,3];
function removeDuplicate(arr){
let newArrr=[];
for(var i=0;i<arr.length;i++){
    if(!newArrr.includes(arr[i])){
        newArrr.push(arr[i]);
    }
}
return newArr;
}
console.log(removeDuplicate(arr))   // output :- [1,2,3,4]

3. Write a JavaScript function to flatten a nested array (depth of 1).
Ans:- let arr=[1,2,3,[1,2],[4,5,6],3];
function flattenArray(arr){
    let newArr=[];
    for(var i=0;i<arr.length;i++){
        if(Array.isArray(arr[i])){
            for(var j=0; j < arr[i].length; j++){
                newArr.push(arr[i][j]);
            }
        }else{
            newArr.push(arr[i]);
        }
    }
    return newArr;
}
console.log(flattenArray(arr))   // output :- [ 1, 2, 3, 1, 2, 4, 5, 6, 3]

4. Write a function to check if a given string is a palindrome.
Ans:- 
function isPalindrome(str) {
    var i = 0;
    var j = str.length - 1;
    var flag = true;
    while (i <= j) {
        if (str.charAt(i) == str.charAt(j)) {
            i++;
            j--;
        } else {
            flag = false;
            break
        }
    }
    return flag;
}
console.log(isPalindrome('naman'));   //true

5. Write a function to find the longest word in a string.
Ans:- 

function longestString(str) {
    let arr = str.split(' ');
    let longestWord = arr[0];
    let maxLength = arr[0].length;
    for (var i = 0; i < arr.length; i++) {
        if (arr[i].length > maxLength) {
            maxLength = arr[i].length;
            longestWord = arr[i];
        }
    }
    return longestWord;

}
console.log(longestString('Hello Welcome to mumbai'));   //Welcome



### Output-Based Questions

1. `console.log(1 + '1'); // What will this output?`
Ans:- 11


2. `let x = 10;
if (true) { 
    let x = 20; 
    console.log(x); // What will this output?
}
console.log(x); // What will this output?`

Ans:- 20, 10


3. `const arr = [1, 2, 3];
arr.push(4);
console.log(arr); // What will this output?`

Ans:- [1, 2, 3, 4]


4. `let a = 5;
let b = a;
a = 10;
console.log(a, b); // What will this output?`

Ans:- a=10,b=5


5. `console.log(typeof null); // What will this output?`
Ans:- object
6. `console.log(typeof undefined); // What will this output?`
Ans:- undefined

7. `let person = { name: 'John' };
const changeName = (obj) => { obj.name = 'Doe';
}
changeName(person);
console.log(person.name); // What will this output?`
Ans:- Doe


8. `let foo = 'foo';
{ let foo = 'bar'; console.log(foo); // What will this output?
}
console.log(foo); // What will this output?`
Ans:- bar, foo


9. `console.log('Hello' || 'World'); // What will this output?`
Ans:- Hello
10. `console.log('' && 'Hello'); // What will this output?`
Ans:- 

