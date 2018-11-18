
:grep

    uses grep | ack on unix boxes
    uses findstr on windows boxes

    

:vimgrep 

    uses vim regex, slower

Usage

    :grep /s /n "foo" *.md
    :vimgrep /foo/ */**/*.md
    
    :copen
    :cclose
    :cnext
    :cprev


Question

What is the quickfix list? 

How do we get to the quickfix list?

* we navigate it with :cnext and :cprev
* we view the quickfix window with :copen and close it with :ccl

What is the equivalent of grep/ack on Windows?

findstr /n "foo" *.md



