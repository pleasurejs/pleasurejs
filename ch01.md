
##What it has & What it does
* Function with arguments
* Arrays

###Requirement of Model
* Add todos
* Delete todos
* Mark todos completed
* Filter Todos like active, completed, all etc.

Convert all of the above requirement into "HAS" and "DOES".

###What it HAS
* todos

```javascript
var todos = [];
```

###What it DOES
* addTodo(item)
* deleteTodo(item)

```javascript
function addTodo(item) {
  todos.push(item);
  console.log("--------Todos list----------");
  console.log(todos);
}
```

Testing add todo

```javascript
addTodo("wake up at 5 AM");
addTodo("do yoga for 1 hr");
```
Deleting of todo

```javascript
function deleteTodo(item) {
  var index = todos.indexOf(item);
  todos.splice(index, 1);
  console.log("--------Todos list----------");
  console.log(todos);
}
```

We see a common pattern in add todo and delete todo, like a recipee, lets refactor it

```javascript
function addTodo(item) {
  todos.push(item);
  logTodos();
}

function deleteTodo(item) {
  var index = todos.indexOf(item);
  todos.splice(index, 1);
  logTodos();
}

function logTodos() {
  console.log("--------Todos list----------");
  console.log(todos);
}
```

Testing delete todo

```javascript
deleteTodo("wake up at 5 AM");
```
We cant fulfill the other requirements straight away as we are passing string as item to addTodo and deleteTodo function. We need something else. Objects!


