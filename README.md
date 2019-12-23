INTRODUCTION

* I simplify [pymake](https://github.com/mozilla/pymake) by keeping its makefile parser only (fix import problem).
* to install, try `git clone https://github.com/cyruscyliu/pymake.git && cd pymake && sodu -H pip3.7 install .`

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
