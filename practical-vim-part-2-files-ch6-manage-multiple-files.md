# Part 2: Files

Progress: 

* Currently at location 3235 in Practical Vim at https://read.amazon.com/ 
* I did not finish the sections on Tabs, because those are a low priority right now.

# buffer list

* buffer: in memory representation of a file
* most vim commands operate on a buffer
* some vim commands operate on a file
  * :write, :update, :saveas
* load many files into the buffer
  * `vim *.txt`
* buffers are not a good way to orgnize our workspace,
* instead, use split windows, tab pages, and the argument list.

## Some Basic Commands

    :bnext
    :ls
    Ctrl + ^
    :buffer {number|pathspec} 

## Suggestions

Consider using Tim Pope's unimpaired.vim plugin to map these: 

    :bnext
    :bprev
    :bfirst
    :blast
  
## Questions

How to remove a file from the buffer list?

    :bdelete n1 n2 n3 n4
    :n,m bdelete

How to rename a file from Vim?

# argument list 

* is more powerful than the buffer list

Some basic commands

    :args

Args works with backtick expansion and with one or more globs.

    :args `some-cli-command`
    :args *.js *.css
    :args **/*.js **/*.cs

buffer list is messy, argument list is tidy workspace

:args {}
:next
:prev
:argdo

## Managing Hidden Files

buffer annotations:

* + modified
    * :write // save
    * :edit! // update from disk
* h hidden
* a active
* %
* #

on :quit, 
* vim will warn and 
* then activate the next modified buffer
* we can choose to :write or :edit! the buffer
* repeat until we've handled all of them

to streamline this, we can use: 
* qall! // quit our vim session, saving no buffers.
* wall  // quit our vim session, saving all buffers.

Change a collection of buffers with a single command

* :argdo
* :bufdo
* :cfdo

# split windows

Ctrl + w + s
Ctrl + w + v
Ctrl + w + w // cycle among windows
Ctrl + w + [hjkl]

:split {file}
:vsplit {file}

:close // close active window
:only  // close all but active window

Ctrl + w + = // equal width and height for all
Ctrl + w + _ // maximize height of active
Ctrl + w + | // maximize width of active

N Ctrl + w + _ // set height of active to N
N Ctrl + w + | // set width of active to N

## tabs (aka tab pages)

collections of windows

similar to virtual desktops in Windows/Linux

vim 
    buffer list
    arg list
    buffer
    window (display a buffer)
    tab (contain windows)

:lcd {path} // set the active window's working directory

:windo {command} // change a collection of windows e.g. with :lcd

:tabedit {file}
