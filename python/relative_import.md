# Python import

## Assuming directory structure below

```
   package/
    __init__.py
    subpackage1/
        __init__.py
        moduleX.py
    moduleA.py
 ```

Python files can be loaded in 2 ways:

- as the top-level scripts like `python myTest.py`
- as a module `python -m pip install pip-tools`

when loaded as top-level scripts

- the logic in __main__ get executed immediately
- its __name__ is set to __main__ even if it's part of module like `moduleA.py`
- cannot use relative import as package structure not known

when loaded as a module

- its __name__ is set according to package structures like `package.subpackage1.moduleX`
- python rule:
  - if a module's name has no dots, it is not considered to be part of a package.
  - relative import use module's name to determine where is it in the package
- when loaded as module, we can use relative import such as `import ../ModuleA`

In order for python interpret to locate the package, the package directory must be accessible from Python module search path (`sys.path`)
