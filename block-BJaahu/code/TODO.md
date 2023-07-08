### For single question we need the following data and methods:

- Data:
  - `title` (title of the question)
  - `options` (array of options)
  - `correctAnswerIndex` (index of the correct option)
- Methods:
  - `isAnswerCorrect` (will accept the index and returns `true` or `false` based on the answer is correct or not)
  - `getCorrectAnswer` (will return the correct answer of the quiz when the function is called)

### Create the object using the following ways

For each different ways of creating object write different solutions.

- Prototypal pattern of object creation (Put methods inside an object and create object using Object.create)
  let methods = {

    iscorrectanswer: function(index){
        return index === this.correctanswerindex
    },
    getcorrectanswer: function(){
        return this.options[this.correctanswerindex]
    }
    
    }

function questions(title,options,correctanswerindex){

let question = Object.create(methods)
question.title = title;
question.options = options;
question.correctanswerindex = correctanswerindex
return question
}



const firstquestion = questions(
"what is capital of jordan",
["Tashkent","Amaan","Nairobi","Kuwait City"],
1
)
- Pseudoclassical Pattern (Put methods inside F.prototype and use `new` to call function)
- questions.prototype = { 

    iscorrectanswer: function(index){
        return index === this.correctanswerindex
    },
    getcorrectanswer: function(){
        return this.options[this.correctanswerindex]
    }
    
    }

function questions (title,options,correctanswerindex){

this.title = title;
this.options = options;
this.correctanswerindex = correctanswerindex;

}



const firstquestion = new questions(
"what is capital of jordan",
["Tashkent","Amaan","Nairobi","Kuwait City"],
1
)
- Create using class
class question {
    constructor(title,options,correctanswerindex){

        this.title = title;
        this.options = options;
        this.correctanswerindex = correctanswerindex;
    }

    iscorrectanswer(index){
        return index === this.correctanswerindex
    }

    getcorrectanswer(){
        return this.options[this.correctanswerindex]
    }
    
    }




const firstquestion = new question(
"what is capital of jordan",
["Tashkent","Amaan","Nairobi","Kuwait City"],
1
)
- Write test by creating two objects also test both methods.
- ..

### To test use the following data

You can use the data given below. You will also have to change the name of the function while calling them.

```js
let firstQuestion = new Question(
  'Where is the capital of Jordan',
  ['Tashkent', 'Amaan', 'Kuwait City', 'Nairobi'],
  1
);
let secondQuestion = new Question(
  'Where is the capital of Jamaica',
  ['Tashkent', 'Amaan', 'Kingston', 'Nairobi'],
  2
);
```
