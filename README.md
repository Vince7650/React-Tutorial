# React-Tutorial
Getting started
 got you

 const api = axios.create({
   baseURL: 'https://api.coinmarketcap.com/v1/ticker/?limit=10/',
 });
 (async () => {
   const res = await api.get('/name');
   console.log(res);

 })();

 /* 7. Functions */

 // is a procedure which performs a set of tasks or calculates a value

 function square(number) {               //  function.. then name  it.. number is arguments
   return number * number;               // body - statements that define fucntion
 }

 console.log(square(4));                 //16

 var someVar = "Hat";                     //scope refers to the visibility of variables
 function myFun() {                       // if defined before function is is global var
 // var someVar = "Shoes";                 // if vars declared in function aswell as function
                                          //parameters - have local scope
   console.log(someVar);                  //if local and global variable is the same, local
                                          // takes precedence over global
 }

 myFun();                                  //Answer - "Hat"
 console.log(someVar);

 console.log(addSquares(1, 3));           //hoisting
                                          // if nesting occurs the inner function is private
                                          //to its containing outer function

 function addSquares(a, b) {
   function square(x) {                    //square is inner
     return x * x;
   }
   return square(a) + square(b);
 }

 a = addSquares(2, 3); // returns 13
 b = addSquares(3, 4); // returns 25
 c = addSquares(4, 5); // returns 41     //functions are hoisted



 /*8. Hoisting */
 // Hoisting is when variable and function declarations are processed before any code is //
 //  executed.



 // console.log(notDeclared); // Uncaught ReferenceError: notDeclared is not defined

 console.log(definedLater);   //undefined
 var definedLater;
 definedLater = 'I am defined!'
 console.log(definedLater)


 console.log(definedSimulateneously);
 var definedSimulateneously = 'I am defined!' //decalaration and definition
 console.log(definedSimulateneously)           // definitions aren't hoisted


 doSomethingElse();
 function doSomethingElse(){
   console.log('I did it!');
 }


 functionVar();                    // Uncaught TypeError: functionVar is not a function
 var functionVar = function(){
   console.log('I did it!');
 }
