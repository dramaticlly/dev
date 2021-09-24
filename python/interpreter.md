# Python Interpreter

default to python 3

## To know existing python version on start up

```python
import sys; 
print('Python %s on %s' % (sys.version, sys.platform))
```

## To find out python PATH used in shell

```python
print('\n'.join(sys.path))
```