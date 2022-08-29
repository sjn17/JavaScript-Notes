# JavaScript-Notes
My Journey towards learning JS
Day0

day1
//Array Destructuring
//To extract the value of arrays 
// const myArray = ["item1","item2"]
// let [ value1, value2] = myArray;
// console.log("The value of value1 is ",value1)
// console.log("The value of value2 is ",value2)


//What happens if array contains more values
//const myArray = ["item1","item2","item3"]
//let [ value1, value2] = myArray;
//console.log("The value of value1 is ",value1)
//console.log("The value of value2 is ",value2)
//noting changes and it is same

//Condition3

// const myArray = ["item1","item2"]
// let [ value1, value2,value3] = myArray;
// console.log("The value of value1 is ",value1)
// console.log("The value of value2 is ",value2)
// console.log("The value of value3 is ",value3) //undefined


//How to Skip index in array just add ,

// const myArray = ["item1","item2","item3"]
//  let [ value1, ,value2] = myArray;
//  console.log("The value of value1 is ",value1)
//  console.log("The value of value2 is ",value2)

//How to Create an Array using array destructuring
// const myArray = ["item1","item2","item3","item4"]
// let [ value1, value2,...myNewArray] = myArray;
// console.log("The value of value1 is ",value1)
// console.log("The value of value2 is ",value2)
// console.log(myNewArray)

#Objects in JavaScript
//Objects in javascript
//In JavaScript, an object is a standalone entity, with properties and type. Compare it with a cup, for example. A cup is an object, with properties. A cup has a color, a design, weight, a material it is made of, etc. The same way, JavaScript objects can have properties, which define their characteristics.
// objects reference type  
// arrays are good but not sufficient 
// for real world data 
// objects store key value pairs 
// objects don't have index

// how to create objects 

// const person = {name:"Harshit",age:22};
//const person = {
//name: "Shubham",
//age: 22,
 //hobbies: ["sleeping", "listening music"]
//}
//console.log(person);

// how to access data from objects
//Two ways to access value for objects . notation and box notion 
// console.log(person["name"]); //always use "" notation otherwise error as keys are bydefault in string
// console.log(person["age"]);
// console.log(person.hobbies);

// how to add key value pair to objects
//person["gender"] = "male";
//console.log(person); 

// difference between dot and bracket notaion
//Use bracket notation when you want to access properties containing spaces
//Use want to access data from keys containing spaces
//Want to give variable as key 
// const key = "email";
// const person = {
//     name: "harshit",
//     age: 22,
//     "person hobbies": ["guitar", "sleeping", "listening music"]

// }

// console.log(person["person hobbies"]);
// person[key] = "harshitvashisth@gmail.com";
// console.log(person);

// how to iterate object 
// const person = {
//     name: "harshit",
//     age: 22,
//     "person hobbies": ["guitar", "sleeping", "listening music"]
// }

// for in loop 
// Object.keys 

// for(let key in person){
//     // console.log(`${key} : ${person[key]}`);
//     console.log(key," : " ,person[key]);
// }
//Object.keys(person) returns an array
// console.log(typeof (Object.keys(person)));
// const val = Array.isArray((Object.keys(person)));
// console.log(val);

//As it is an array we can iterte it using for of loop
// for(let key of Object.keys(person)){
//     console.log(person[key]);
// }

// computed properties

// const key1 = "objkey1";
// const key2 = "objkey2";

// const value1 = "myvalue1";
// const value2 = "myvalue2";

//How to achive below using the variables
// const obj = {
//     objkey1 : "myvalue1",
//     objkey2 : "myvalue2",
// }
//way1
// const obj = {
//     [key1] : value1,
//     [key2] : value2
// }

//Way2
// const obj = {};

// obj[key1] = value1;
// obj[key2] = value2;
// console.log(obj);

// object destructuring
// const band = {
//     bandName: "led zepplin",
//     famousSong: "stairway to heaven",
//     year: 1968,
//     anotherFamousSong: "kashmir",
//   };
  
//  let {bandName,year,famousSong:var1, ...restProps} = band; //to change the name of variable use var1 if you try to print famousSong you will get a error
//  console.log(bandName,year,var1)

//  //...restprops used to print rest properties
// console.log(restProps);

// objects inside array 
// very useful in real world applications

// const users = [
//     {userId: 1,firstName: 'harshit', gender: 'male'},
//     {userId: 2,firstName: 'mohit', gender: 'male'},
//     {userId: 3,firstName: 'nitish', gender: 'male'},
// ]
// for(let user of users){
//     console.log(user.firstName);
//     console.log(user.userId);
// }
Day 2
//A function is a set of statements that take inputs, do some specific computation, and produces output.
// Basically, a function is a set of statements that performs some tasks or does some computation and then return the result to the user.
//Function Declaration
// function PrintGM(){
//     console.log("Good morning")
// }

// PrintGM()

// function ReturnFirstCharacter(str){
//     return str[0];
// }

// console.log(ReturnFirstCharacter("shubham"));

// function Target(array,target){

//     for(i=0; i< array.length; i++){
//         if(array[i] === target){
//             return i;
//         }
//     }
//     return -1;


// }
// console.log(Target([1,3,3,4],3))

//Function Expression

// const PrintGM = function(){
//     console.log("Good morning")
// }

// PrintGM()
//Arrow Functions

// const PrintGM = ()=>{
//     console.log("Good morning")
// }

// PrintGM()


// const ReturnFirstCharacter=(str)=>{
//     return str[0];
// }

// console.log(ReturnFirstCharacter("shubham"));

// const Target=(array,target) => {

//     for(i=0; i< array.length; i++){
//         if(array[i] === target){
//             return i;
//         }
//     }
//     return -1;


// }
// console.log(Target([1,3,3,4],3))
//If arrow function contains only one Parameter you can remove ()

//IF function returns only one line you can write is as follows
//const ReturnFirstCharacter=str=> str[0];


//Hoisting
//JavaScript Hoisting refers to the process whereby the interpreter appears to move the declaration of functions, variables or classes to the top of their scope, prior to execution of the code. 
//Hoisting allows functions to be safely used in code before they are declared
//It only work for normal function does n't work with arrow functions and function expressions

// PrintGM()
// function PrintGM(){
//     console.log("Good morning")
// }
//You will get an erro while using it with arrow Functions
// PrintGM()
// const PrintGM = ()=>{
//          console.log("Good morning")
//      }
// console.log(a)
// var a = 2
// console.log(a)

// console.log(b) //You will get error with let or const
// let b = 3

// let a ="hell";
// console.log(a) //Error Uncaught SyntaxError: Identifier 'a' has already been declared (at function.js:90:5)

// functions inside function 
// function app(){
//     const myFunc = () =>{
//         console.log("hello from myFunc")
//     }
    
//     const addTwo = (num1, num2) =>{
//         return num1 + num2;
//     }

//     const mul = (num1, num2) => num1* num2;

//     console.log("inside app");
//     myFunc();
//     //console.log(addTwo(2,3));
//     //console.log(mul(2,3));
// }
// app();

//myFunc() // Cannot be called outside the main Function

//Lexical Scope

// A lexical scope in JavaScript means that a variable defined outside a function can be accessible inside another function defined after the variable declaration.
//  But the opposite is not true; the variables defined inside a function will not be accessible outside that function.

//Case1
//  function myApp(){

// const myVar = "value1"

//  const myFunc=()=>{
// const myVar = "value59"
// console.log(myVar);
// }

// console.log(myVar);
// myFunc()


// }
// myApp()

//Case2
// function myApp(){

//     const myVar = "value1"
    
//      const myFunc=()=>{
//     //const myVar = "value59"
//     console.log(myVar); //Value is taken outside the lexical Scope
//     }
    
//     console.log(myVar);
//     myFunc()
    
    
//     }
//     myApp()
    

//Case4
// const myVar = "value1";

// function myApp(){
    

//     function myFunc(){
//        
//         const myFunc2 = () =>{
//             console.log("inside myFunc", myVar);//Vakue is taken from Global Environment
//         }
//         myFunc2();
//     }


//     console.log(myVar);
//     myFunc();
// }

// myApp()

//Block Scope Vs Function Scope
// let and const are block scope
// var is function scope 


// {
//     let name = "Shubham";
//     console.log(name)
// }
// console.log(name)

// {
//     var name = "Shubham";
    
// }
// console.log(name)

//Declaring and acessing using var
// console.log(name)
// {
//     var name = "Shubham";
    
// }
// console.log(name)

//var is function Scope
// function myApp(){
//     if(true){
//         var firstName = "rohit";
//         console.log(firstName);
//     }

//     if(true){
//         console.log(firstName);
//     }
//     console.log(firstName);
// }



//Using var
// console.log(firstName)
// {
//     var firstName = "Rohit";
// }
// console.log(firstName)
// {
//     var firstName = "Sunil";
// }
// console.log(firstName)
//Please see the output in browser console to see the error
// function test(){

//     if(true){
//         let firstName = "Sunil";
//         console.log(firstName);
//     }
// console.log(firstName)
// }

// test()

//Var gives no error
// function test(){

//     if(true){
//         var firstName = "Sunil";
//         console.log(firstName);
//     }
// console.log(firstName)
// }

// test()

// nested destructuring 
//Use {}symbol to destructure individual object
// const users = [
//     {userId: 1,firstName: 'harshit', gender: 'male'},
//     {userId: 2,firstName: 'mohit', gender: 'male'},
//     {userId: 3,firstName: 'nitish', gender: 'male'},
// ]

// const [{firstName: user1firstName, userId}, , {gender: user3gender}] = users;
// console.log(user1firstName);
// console.log(userId);
// console.log(user3gender);
