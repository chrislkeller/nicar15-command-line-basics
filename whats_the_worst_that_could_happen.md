# What's the worst that could happen?

One of the toughest challenges when learning how interactive shells work is knowing what to do when you get stuck.  The purpose of this document is to provide some general advice on how to get *un*-stuck, and some additional caveats.

* `^c`: this is the representation of what you get when you press `control`+`c` on your keyboard at the same time.  `^c` is used to interrupt and halt whatever command is currently running.  `^c` is often used within other specialized interactive programs (such as Ruby, Python, or other interactive programming language environments) to halt the currently running command, but remain w/in that programming environment.
* `^d`: this is the representation of what you get when you press `control`+`d` on your keyboard at the same time.  `^d` is used to immediately terminate whatever program is currently running and exit to the command line.  Do not pass 'go' do not collect 200$.  If you are inside another interactive program, `^d` will terminate that program.

## mismatching parentheses, quotes and other characters that can screw up your instructions

[Explain & and how quoting works]