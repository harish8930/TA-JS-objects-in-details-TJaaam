## Create Class

Convert the give image into class using inheritance.

- `name` is the property
- `eat()` is the method

Property ending with `()` is method. And others are properties.

![Inheritance](../assets/inheritance.png)

class Person{
constructor(name,age,gender){
  this.name = name;
  this.age = age;
  this.gender = gender;
}
eat(){
  console.log(` My name is ${this.name} my age is ${this.age} and i am ${this.gender} and i can eat`)
}

sleep(){
  console.log(`${this.name} and i can sleep`)
}

walk(){
  conmsole.log(`${this.name} and i can walk`)
}
}


class Player extends Person{
  constructor(name,age,gender,sportsname){
  super(name,age,gender)
    this.sportsname = sportsname
  }

  play(){
    console.log(` My name is ${this.name} i can play`)
  }
  
 

}


class Teacher extends Person{
  constructor(name,age,gender,institutename){
  super(name,age,gender)
    this.institutename = institutename
  }

  teach(){
    console.log(` My name is ${this.name} i can teach`)
  }
}

class Artist extends Person{
  constructor(name,age,gender,kind){
  super(name,age,gender)
    this.kind = kind;
  }

  CreateArt(){
    console.log(` My name is ${this.name} i can createart`)
  }
}

class Cricketer extends Player{
  constructor(name,age,gender,sportsname,teamname){
  super(name,age,gender,sportsname)
    this.teamname = teamname
  }

  playCricket(){
    console.log(` My name is ${this.name} i can play Cricket`)
  }

}
