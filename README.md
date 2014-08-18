next-todo.txt
=============

Identifies and labels next actions as +next in in a tab indented [todo.txt](http://todotxt.com/) file. 
Priorities and projects are inherited by next actions, if they have none already.

This program assumes that

* Each root (unindented) task has only **one** next action own task tree
* The next action for each task tree will have no subtasks
* The next action will have no sibling tasks listed higher in the same task tree


## Usage

Organize your todo.txt into a tab indented outline, similar to
  
    (A) Walk the dog +dog
    	put on the collar
	    	buy a collar
	    put on the leash
		    buy a leash
    Read a book
	    (B) go the library
		    get directions to library
	    choose a book
	    sit in a chair 
	
label next actions with the following command

  $ todo.sh next

Your todo.txt will now be 

    (A) Walk the dog +dog
	    put on the collar
		    (A) buy a collar +dog +next
    	put on the leash
	  	buy a leash
    Read a book
	    (B) go the library
		    (B) get directions to library +next
	    choose a book
	    sit in a chair 
	
Display next actions by with either
  
    $ todo.sh ls +next

Or
  
    $ todo.sh lsn
  
for the following output

    03 (A) buy a collar +dog +next
    08 (B) get directions to library +next
    --
    TODO: 2 of 10 tasks shown
  
To show all tasks


## Installation

Put next, lsn, and lsna in your addon directory, following directions on the [todo.txt project page](https://github.com/ginatrapani/todo.txt-cli/wiki/Todo.sh-Add-on-Directory#installation)

lsn may be renamed to ls for convenience to override ls.

## Files

* **next**: finds and labels next actions in outline with +next and inherited priority and project list

Because the default list function does remove whitespace from indented tasks, the following list functinos are provided
* **lsna**: like ls, but removes leading white space from tasks for better display of items contained in an outline
* **lsn**: like lsna +todo. Removes whitespace

the list functions preserve highlighting
