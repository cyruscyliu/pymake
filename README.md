INTRODUCTION

* I simplified [pymake](https://github.com/mozilla/pymake) by keeping its makefile parser only (I fixed the import problems).
* Python3

USAGE
```python
from pymkparser import parser

def example(path_to_makefile):
    with open(path_to_makefile) as f:
        lines = f.readlines()
    stmts = parser.parsestring(''.join(lines), path_to_makefile)
    
    for stmt in stmts:
        do_your_anaysis(stmt);
```
