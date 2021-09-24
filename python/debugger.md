# python debugger

## debug a python standalone script

```shell
python -m pdb myscript.py
```

## debug a python module

```shell
python -m pdb -m mymodule.cli
```

## debug within the python src code

```python
import pdb

def make_bread():
    pdb.set_trace()
    return "I don't have time"

print(make_bread())
```

if you are using Python 3.7+ then you can simply use the breakpoint() [built-in function](https://docs.python.org/3/library/functions.html#breakpoint). It automatically imports pdb and calls pdb.set_trace().

## Within pdb

`?` will show command reference, here's list of common commands

```python
(Pdb) ?c
c(ont(inue))
        Continue execution, only stop when a breakpoint is encountered.

(Pdb) ?w
w(here)
        Print a stack trace, with the most recent frame at the bottom.
        An arrow indicates the "current frame", which determines the
        context of most commands.  'bt' is an alias for this command.
```

if needs more detailed description

```python
"help pdb" shows the full pdb documentation
```
