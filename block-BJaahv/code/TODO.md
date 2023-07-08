# 🎖 Object Creation Patterns

Create a object using the following patterns given below.

## Create in all 4 formats

- [ ] Using function to create object
    function createUser(name,id,nofproject){
let user = {};
user.name = name ;
user.id = id;
user.nofproject = nofproject;



user.getproject = function(){
    return user.nofproject;
}
user.changename = function(newName){
    let previousname = user.name;
    user.name = newName;
    return previousname;

}

user.incrementProject = function(){
    user.nofproject += 1
    return user.nofproject;
}

user.decrementProject = function(){
user.decrementProject -= 1
return user.nofproject

}
 return user;

}

- [ ] Using Object.create (prototypal pattern)
  let method = {
getproject:function(){
    return this.nofproject;
},

changename :function(newName){
    let previousname = this.name;
    this.name = newName;
    return previousname;

},

incrementProject: function(){
    this.nofproject += 1
    return this.nofproject;
},

decrementProject:function(){
this.decrementProject -= 1
return this.nofproject
}


}







function createUser(name,id,nofproject){
let user = Object.create(method);
user.name = name ;
user.id = id;
user.nofproject = nofproject;
 return user;

}



let user1 = createUser("harry","007","100")

- [ ] Using Pseudoclassical Way
  createUser.prototype = {
getproject:function(){
    return this.nofproject;
},

changename :function(newName){
    let previousname = this.name;
    this.name = newName;
    return previousname;

},

incrementProject: function(){
    this.nofproject += 1
    return this.nofproject;
},

decrementProject:function(){
this.decrementProject -= 1
return this.nofproject
}


}

function createUser(name,id,nofproject){
this.name = name ;
this.id = id;
this.nofproject = nofproject;
}
- [ ] Using Class

class user {
    constructor(name,id,nofproject){
this.name = name ;
this.id = id;
this.nofproject = nofproject;
}


getproject(){
    return this.nofproject;
}

changename(newName){
    let previousname = this.name;
    this.name = newName;
    return previousname;

}

incrementProject(){
    this.nofproject += 1
    return this.nofproject;
}

decrementProject(){
this.decrementProject -= 1
return this.nofproject
}

}


let user1 = new user("harry","007",100)

## Requirements

Create User (class/function) with the following properties.

- [ ] properties (data):
  - [ ] name
  - [ ] id
  - [ ] noOfProjects
     
- [ ] methods:
  - [ ] getProjects -> return number of project
  - [ ] changeName -> accepts one parameter (newName)returns old user name
  - [ ] incrementProject -> returns updated number of projects
  - [ ] decrementProject -> returns updated number of projects
...
Write 2 tests for all the different ways of creating object. Test all the methods on these objects.
