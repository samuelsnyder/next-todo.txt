next-todo.txt
=============

Identifies and displays next actions in a tab indented [todo.txt](http://todotxt.com/) file. 

This program assumes that

* Each root (unindented) task has only **one** next action own task tree
* The next action for each task tree will have no subtasks
* The next action will have no sibling tasks listed higher in the same task tree


## Usage

Organize your todo.txt into a tab indented outline, similar to
  
    Walk the dog
    	put on the collar
	    	buy a collar
	    put on the leash
		    buy a leash
    Read a book
	    go the library
		    get directions to library
	    choose a book
	    sit in a chair 
	
next actions will be displayed as

    $ todo.sh next
    03 buy a collar
    08 get directions to library
    --
    TODO: 2 of 10 tasks shown
  

## Installation

Put **next** in your addon directory, following directions on the [todo.txt project page](https://github.com/ginatrapani/todo.txt-cli/wiki/Todo.sh-Add-on-Directory#installation)
