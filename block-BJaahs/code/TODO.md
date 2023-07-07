If we want to build any app the two most important thing to think about is Data and Behavior. So for our quiz app let's break it down. To make a quiz app we need to create Single Question object.

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

- Without Object
  let question = "what is capital or india?"
  let options = [mumbai,kolkata,delhi,surat];
  //method for this

  function isanswerCorrect(){
  if(option.index[2]){
  return true;}else{
  return false;
  }
  }
  function getcorrectAnswer(){
  rerturn options.index[2]
  }
  
- Organize using object
let obj = {
   question :"what is capital or india?"
   options : [mumbai,kolkata,delhi,surat];
isanswerCorrect: function(){
  if(option.index[2]){
  return true;}else{
  return false;
  }
  }
getcorrectAnswer:  function getcorrectAnswer(){
  rerturn options.index[2]
  }
}

- Use a function to create object
function quiz(){
let obj ={};
obj.question = question;
obj.options = options;

obj.isanswerCorrect = function(){
  if(options.index[]){
  return true;}else{
  return false;
  }
  }
obj.getcorrectAnswer:  function(){
  rerturn options.index[]
  }

- Convert the function to use `this` keyword
function quiz(){
let obj ={};
obj.question = question;
obj.options = options;

this.isanswerCorrect = function(){
  if(options.index[]){
  return true;}else{
  return false;
  }
  }
this.getcorrectAnswer:  function(){
  rerturn options.index[]
  }








- Write test by creating two objects also test both methods.

### To test use the following data

```js
const testData = {
  title: 'Where is the capital of Jordan',
  options: ['Tashkent', 'Amaan', 'Kuwait City', 'Nairobi'],
  correctAnswerIndex: 1,
};
```
