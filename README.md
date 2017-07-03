# NodeJS Command Line Todo Manager

## Features

* Simple CLI API
* Via single `todos.js` script
* Database in `.json`. file
* Outputs current state after every command

## Functionality

### Add a task

Use `add {text}` command.

```
$ node todo.js add "Buy more juice"
$ node todo.js add "Go for a walk with the ferret"
$ node todo.js add "Time to finish the picture"
```

### List tasks

Run without arguments. Logs the list of unarchived tasks.

```
$ node todo.js
[ ] 1. Buy more juice
[ ] 2. Go for a walk with the ferret
[ ] 3. Time to finish picture
```

### Complete a task

Use `done {id}` command.

```
$ node todo.js done 1
[X] 1. Buy more juice
[ ] 2. Go for a walk with the ferret
[ ] 3. Time to finish picture
```

### Delete a task

Use `delete {id}` command.

```
$ node todo.js delete 1
[ ] 2. Go for a walk with the ferret
[ ] 3. Time to finish picture
```

### Archive tasks

User `archive` command. Archived tasks are possible to view only in database file.

```
$ node todo.js archive
= Add a task! =
```

## Database

### todos.json

```json
[
   {
    "text": "Go for a walk with the ferret",
    "status": "active"
   },
   {
    "text": "Time to finish picture",
    "status": "done"
   },
   {
    "text": "Buy more juice",
    "status": "archived"
   }
]
  ```
  
### Item states

```js
{status: "active"}
{status: "done"}  
{status: "archived"}
```
