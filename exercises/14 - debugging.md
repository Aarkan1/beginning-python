## Exercise 14: debugging

* Create a python file and add the following code:

  ```py
  import pdb

  with open('files/words.txt') as f:
      for line in f:
          #line = line.rstrip()
          pdb.set_trace()
          if len(line) == 1:
              continue
          if line[::-1] == line:
              print(line)
  ```

* By removing the line saying `line = line.rstrip()` we introduce a bug  into the program. `pdb.set_trace()` starts the debugger.
* Run the program. This will take you into an interactive debugger.
* The debugger has stopped at the line `if len(line) == 1:` &mdash; let's make
  sure the length is not 1. Type `len(line)`.
* That should be fine, so let's type `n` to go to the next statement.
* Now we're at `if line[::-1] == line:` &mdash; type `line` to check what `line`
  contains.
* A-ha! Now we see the offending line break character. That must be what's causing the bug!
* If you want, type `h` to get a list of some other commands you can use while
  in the debugging shell.
* Type `q` to end the debugging session.
* Go back into the file and re-add the `line = line.rstrip()` line. You can also
  remove the `import pdb` line and the `pdb.set_trace()` line now.
* Re-run the program to see it work correctly.

