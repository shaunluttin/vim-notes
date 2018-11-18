

# How To

Some how to items in the order that I discover them.

### Find and Replace

    %s/find/replace/flag

### Trim Trailing Whitespace

    %s/\s\+$//g

### Create a new file

    // create a new buffer in the current window
    :enew

    // save it as
    :save <name>

### Unload a buffer

    :bd

### Turn on spell check

    set spell

### Remove a file from the args list

    :argd

### Add one or more files to an existing arg list

    :argadd {files}
    :argedit {files}

### Change the arg list

    :args {files}

### List Buffers

    :args
    :buffers | :ls

### Activate a buffer

    :buffer <file>
    :buffer <index>

### Maximize a window

    <C-w>_  // height
    <C-w>|  // width
    :only   // close all but active

### Rename a file

See https://stackoverflow.com/a/1205382/1108891

    :Ex    // opens the explorer
    :Sex   // opens the explorer in a split window
    <C-R>  // renames the current file


