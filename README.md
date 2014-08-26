next-todo.txt
=============

Identifies and displays **[next actions](http://en.wikipedia.org/wiki/Getting_Things_Done)** and inherited priorities and projects in a tab indented [todo.txt](http://todotxt.com/) file. 

**Rules for determining next actions**
* Each root (unindented) task has only **one** next action own task tree
* The next action for each task tree will have no subtasks
* The next action will have no sibling tasks listed higher in the same task tree

Projects (e.g. *+projectexample*) and priority (e.g. *(A)*) are inherited from the root (unindented) task.

## Usage

Organize your todo.txt into a tab indented outline, similar to
    
    $ cat -n todo.txt     
    1  (A) Walk the dog +pets
    2          put on the collar +collar
    3                  buy a collar @petstore
    4          put on the leash +leash
    5                  buy a leash
    6  (A) Read a book +read
    7          (B) go the library
    8                  get directions to library
    9          choose a book
    10          sit in a chair
	
next actions will be displayed as (with color coding)

    $ todo.sh next
    03 (A) buy a collar @petstore +pets +collar
    08 (B) get directions to library +read
  
## Installation

Put **next** in your addon directory, following directions on the [todo.txt project page](https://github.com/ginatrapani/todo.txt-cli/wiki/Todo.sh-Add-on-Directory#installation)
