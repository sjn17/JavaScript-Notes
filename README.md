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
