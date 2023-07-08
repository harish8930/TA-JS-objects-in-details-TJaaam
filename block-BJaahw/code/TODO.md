1. Create a function `createUser` that accepts `name` and `age` and returns a new object with those properties.
function createUser(){
let user = {}
user.name = name;
user.age = age;
return user;
user.function(){
alert(`Welcome ${user.name}`
}
3. Add a method named `sayHello` inside the object created above. When called it should alert `Welcome {user}`. Replace `{user}` with the name of the user.
function createUser(name,age){
    let user = {sayhello:function(){
        alert(`welcome ${name}`)
    }};
    user.name = name;
    user.age = age;
return user;
}
let newUser = createUser("harry",25);
newUser.sayhello();
4. Use the data (name, age) of two different person to create the object using `createUser`. Store the returned value in `personOne` and `personTwo`.
function createUser(name,age){
    let user = {sayhello:function(){
        alert(`welcome ${name}`)
        
    }};
    user.name = name;
    user.age = age;

return user;
}
let person1 = createUser("harry",25);
let person2 = createUser("johnson",27);

5. Change the code inside `createUser` in such a way that the methods `sayHello` doesn't have to be in all object. Use the prototypal nature. (Hint Object.create())
function createUser(name,age){
    let user = Object.create(method)
    user.name = name;
    user.age = age;

return user;

}
let method = {
     sayHello(){
alert(`Welcome ${user.name}`)
    }

}
let person1 = createUser("harry",25);
let person2 = createUser("johnson",27);

6. Convert the `createUser` function into Pseudoclassical pattern of object creation. Use `F.prototype` to store the methods. `F.prototype` means storing the methods in prototype property of the function.

function createUser(name,age){
    let user = Object.create(createUser.prototype)
    user.name = name;
    user.age = age;

return user;

}
createUser.prototype = {
     sayHello(){
alert(`Welcome ${user.name}`)
    }

}
let person1 = createUser("harry",25);
let person2 = createUser("johnson",27);


7. Use `new` to create two new objects with the data of two different person and re-assign the value of `personOne` and `personTwo`.
function createUser(name,age){
    this.name = name;
    this.age = age;

}

createUser.prototype = {
     sayHello: function(){
alert(`Welcome ${this.name}`)
    }
}


 

let person1 = new createUser("harry",25);
let person2 =  new createUser("johnson",27);

8. Try calling `personOne.sayHello()` and `personTwo.sayHello()`. Check if you get the required output.
person1.sayHello();
person2.sayHello();
10. Convert the `createUser` function into `User` class.
class CreateUser{
    constructor(name,age){
    this.name = name;
    this.age = age;
    }
 sayHello(){
        alert(`Welcome ${this.name}`)   }    
}



let person1 = new CreateUser("harry",25);
let person2 =  new CreateUser("johnson",27);

11. Check by creating two instance of the class using data of two different persons and re-assign the value of `personOne` and `personTwo`

12. Try calling `personOne.sayHello()` and `personTwo.sayHello()`. Check if you get the required output.
