
> Progress: Currently at location 3033 in Practical Vim at https://read.amazon.com/ 

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

# split windows
