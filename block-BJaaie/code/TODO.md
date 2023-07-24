# Inheritance.

Convert the below requirements into inheritance using:

- Pseudoclassical Pattern
- Class Pattern

#### Animal

Properties:

- `location`
- `numberOfLegs`

Methods

- `eat()` - log a message saying `I live in ${location} and I can eat`

- `changeLocation(newLocation)` - accepts location and updates the location of the animal

- `summary()` - returns `I live in ${location} and I have ${numberOfLegs}`

#### Dog

It will have all the properties and methods of the Animal. These are the extra properties and methods these dogs will have.

Properties:

- `name`
- `color`

Methods:

- `bark()` - alerts a message saying `I am ${name} and I can bark 🐶`
- `changeName(newName)` - accepts the name property and updates the name of the dog
- `changeColor(newColor)` - accepts the new color and updates the color of the dog
- `summary()` - returns `I am ${name} and I am of ${color} color. I can also bark`

#### Cat

It will have all the properties and methods of the Animal. These are the extra properties and methods these dogs will have.

Properties:

- `name`
- `colorOfEyes`

Methods:

- `meow()` - alerts a message saying `I am ${name} and I can do mewo meow 😹`

- `changeName(newName)` - accepts the name property and updates the name of the dog

- `changeColorOfEyes(newColor)` - accepts the new color and updates the color of the dog

- `summary()` - returns `I am ${name} and the color of my eyes are ${colorOfEyes}. I can also do meow meow`

// inheritance using class
class Animal{
constructor(location,numberoflegs){
this.location = location;
this.numberoflegs = numberoflegs
}
eat(){
  console.log(`I live in ${this.location} and i can eat`)
}

changelocation(newloaction){
this.location = newloaction
return this.location
}

summary(){
  return `i live in ${this.location} and i have ${this.numberoflegs}`
}
}


class Dog extends Animal{
constructor(location,numberoflegs,name,color){
  super(location,numberoflegs)
  this.name = name;
  this.color = color;
}
bark(){
  alert(`I am ${this.name} and I can bark`)
}
changename(newName){
this.name = newName;
return this.name ;
}
changecolor(newcolor){
  this.color = newcolor
  return this.color;
}

summary(){
  return `I am ${this.name} and I am of ${this.color} color. I can also bark`
}
}

class Cat extends Dog {
constructor(location,numberoflegs,name,colorOfEyes){
  super(location,numberoflegs)
  this.name = name 
  this.colorOfEyes =colorOfEyes;
}
meow(){
  alert(`i am {this.name} and i can do meow meow` )
}

changeName(name ){
this.name = name 
return this.name;
}

changecolorofeye(newcolor){
this.colorOfEyes = newcolor
return this.colorOfEyes
}
summary(){
  return `i am ${this.name} and i am from${this.location} and the color of my eyes ${this.colorOfEyes}`
}

}









