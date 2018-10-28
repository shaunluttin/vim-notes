
### What are the primary differences between the buffer list and the args list?

    buffer list                        args list

    for the entire Vim session         for the active window

    vertical list of buffers           horizontal list of buffers

    view with :ls                      view with :args

    :bufdo {command}                   :argdo {command} 
      :bufdo :w                          :argdo :w

    change with ???                    change with :args {files}

    navigate with                      
      :bnext                           :next
      :bprev                           :prev
