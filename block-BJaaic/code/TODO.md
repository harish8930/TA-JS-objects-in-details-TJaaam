# Inheritance

Convert the below requirements into inheritance using prototypal patters.

#### Animal

Properties:

- `location`
- `numberOfLegs`

Methods

- `eat()` - log a message saying `I live in ${location} and I can eat`

- `changeLocation(newLocation)` - accepts location and updates the location of the animal

- `summary()` - returns `I live in ${location} and I have ${numberOfLegs}`

#### Dog
et animalMethod ={
eat: function(){
  console.log(`I Live in ${this.location} and i can eat`)
},
changeLocation: function(newloaction){
  this.location = newloaction;
  return this.newloaction
},
summary: function(){
  console.log(`I live in ${this.location} and i have ${this.nooflegs}`)
}
}


function createanimal(location,nooflegs){
  let obj = Object.create(animalMethod);
  obj.location = location;
  obj.nooflegs = nooflegs;
  return obj;
}

function createDog(location,nooflegs,name,color){
  let obj = createanimal(location,nooflegs);
  Object.setPrototypeOf(obj,dogMethod)
  obj.name = name;
  obj.color = color;
  return obj;
}


let dogMethod = {
bark: function(){
  alert(`I am ${this.name} and i can bark`)
},
changename: function(name){
this.name = name;
return this.name
},
changecolor: function(newColor){
this.color = newColor
return this.color
},
summary: function(){
  return `i am  ${this.name} and i am of ${this.color} color and i can also bark`
},
}
Object.setPrototypeOf(dogMethod,animalMethod)


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
.
