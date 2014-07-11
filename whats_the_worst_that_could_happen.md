# What's the worst that could happen?

One of the toughest challenges when learning how interactive shells work is knowing what to do when you get stuck.  The purpose of this document is to provide some general advice on how to get *un*-stuck, and some additional caveats.

* `^c`: this is the representation of what you get when you press `control`+`c` on your keyboard at the same time.  `^c` is used to interrupt and halt whatever command is currently running.  `^c` is often used within other specialized interactive programs (such as Ruby, Python, or other interactive programming language environments) to halt the currently running command, but remain w/in that programming environment.
* `^d`: this is the representation of what you get when you press `control`+`d` on your keyboard at the same time.  `^d` is used to immediately terminate whatever program is currently running and exit to the command line.  Do not pass 'go' do not collect 200$.  If you are inside another interactive program, `^d` will terminate that program.  `^d` should land you back on your bare command line of your operating system.

## mismatching parentheses, quotes and other characters that can screw up your instructions

Computers are exactingly precise.  At their core they are rules machines, and they are incapable of deviating from those rules.  They do not forget, they do not forgive, all they know is the rules.

So, when you start telling a computer what to do, the computer will listen, focused intently, until you complete what you have started, or you tell it explicitly that you'd like to start over, or stop doing what you you started.  It will continue indifferent to your changes of heart or intent.

An example from the interactive ruby shell (a.k.a. `irb`)
```bash
2.1.2 :001 > puts "hello"
hello
 => nil 
2.1.2 :002 > puts "Hello knowtheory
2.1.2 :003"> 
2.1.2 :004"> omg what is going on
2.1.2 :005"> why won't it just say hello?!?
2.1.2 :006"> why is there a quote next to the command prompt!?
2.1.2 :007"> everything is terrible and i don't know what to do next!
2.1.2 :008"> Oh right.  i should use cntrl+c
2.1.2 :009"> ^C
2.1.2 :009 > puts "I see that the quote in the command prompt is gone now"
I see that the quote in the command prompt is gone now
 => nil 
2.1.2 :010 > puts "it must have been because i forgot the end quote on line 002
2.1.2 :011"> uhoh. i did it again.
2.1.2 :012"> But this time, i'm going to try just ending with a quote"
it must have been because i forgot the end quote on line 002
uhoh. i did it again.
But this time, i'm going to try just ending with a quote
 => nil 
2.1.2 :013 >
```

[Explain & and how quoting works]
