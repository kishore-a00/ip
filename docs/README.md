# Duke User Guide


## Key things to take note:

Write the commands in lower case eg. `todo`

Ensure you have Java 11 on your computer


## Features
Duke is your personal assistant who helps you keep track of tasks.

Duke supports storing 3 types of tasks: `todo`, `deadline` and `event`

Once you are done with a task you can `mark` it or `unmark` a previously marked task

You can `list` all the marked and unmarked tasks that you have

Duke has a `find` feature to allow you to look for tasks in your list

You can `delete` a task once you no longer want it in your list

Best of all, after saying `bye`, Duke still remembers your tasks

Duke supports the following commands: `todo`, `deadline`, `event`, `list`, `mark`, `unmark`, `find`, `delete` and `bye`.


## Usage

### Create a ToDo: `todo`

Creates and stores a todo type of task

Usage: `todo TASK_DESCRIPTION`

Example: `todo Buy apples`

Expexted output:
```
________________________________________
Sure, I've added this task: 
[T] [ ] Buy apples
You have 1 task!
________________________________________
```

### Create a Deadline: `deadline`

Create and stores a deadline type of task

Usage: `deadline TASK_DESCRIPTION /by DUE_DATE`

Example: `deadline CS2113 Homework /by tomorrow`

Expected output:
```
________________________________________
Sure, I've added this task: 
[D] [ ] CS2113 Homework (by: tomorrow)
You currently have 2 tasks in the list.
________________________________________
```

### Create an Event: `event`

Creates and stores an event type of task

Usage: `event TASK_DESCRIPTION /from START_DATE /to END_DATE`

Example: `event Birthday Party /from Tuesday /to Sunday`

Expected output:
```
________________________________________
Sure, I've added this task: 
[E] [ ] Birthday Party (from: Tuesday to: Sunday)
You currently have 3 tasks in the list.
________________________________________
```

### List all tasks: `list`

List all the tasks you have added

Usage: `list`

Example: `list`

Expected output:
```
________________________________________
Here are the tasks in your list:
1. [T] [ ] Buy apples
2. [D] [ ] CS2113 Homework (by: tomorrow)
3. [E] [ ] Birthday Party (from: Tuesday to: Sunday)
________________________________________
```


### Mark a task: `mark`

Mark an unmarked task

Usage: `mark TASK_INDEX`

Example: `mark 3`

Expected output:
```
________________________________________
Great! I've marked it as done!
[X] Birthday Party
________________________________________
```


### Unmark a task: `unmark`

Unmark a marked task

Usage: `unmark TASK_INDEX`

Example: `unmark 3`

Expected output:
```
________________________________________
Alright, I've marked the task as undone.
[ ] Birthday Party
________________________________________
```


### Find tasks: `find`

Find tasks based on a letter, word or phrase
Note that the statement after the find function is case sensitive.

Usage: `find STATEMENT`

Example: `find B`

Expected output:
```
________________________________________
Here are the matching tasks I found: 
1. [T] [ ] Buy apples
2. [E] [ ] Birthday Party (from: Tuesday to: Sunday)
________________________________________
```


### Delete task: `delete`

Delete a task based on its corresponding index

Usage: `delete INDEX`

Example: `delete 3`

Expected output:
```
________________________________________
Alright, I have removed this task: 
[E] [ ] Birthday Party (from: Tuesday to: Sunday)
You currently have 2 tasks in the list.
________________________________________
```


### Save and exit: `bye`

Save all tasks and exit Duke

Usage: `bye`

Example: `bye`

Expected output:
```
I have saved your tasks.
Bye. Hope to see you again soon!
________________________________________
```

## Running Duke for the first time vs subsequent times
### Running Duke for the first time:

As there is no saved text file to load the tasks from. Duke will only create the text file after the command `find` or `bye` is used.
Expected output:
```
________________________________________
Hello! I'm Duke
________________________________________
Please wait, I am attempting to retrieve your saved tasks...
Hmm.. I can't seem to locate a saved file...
No worries, I have just created a new file for you:D
Add your first task!
________________________________________
```

### Running Duke again:

The saved tasks will be loaded the moment you open Duke again.

Expected output:
```
________________________________________
Hello! I'm Duke
________________________________________
Please wait, I am attempting to retrieve your saved tasks...
________________________________________
________________________________________
Here are the tasks in your list:
1. [T] [ ] Buy apples
2. [D] [ ] CS2113 Homework (by: tomorrow)
________________________________________
________________________________________
```
