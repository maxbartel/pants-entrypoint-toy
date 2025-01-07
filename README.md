The working example is running with 

```bash
pants test packages/projA::
```


The broken example is 
```bash
pants test packages/projB::
```


The only difference between those two is the entrypoint.

projA Build file:

```    
entry_points = {
    "test":{"projA": "src.projA.conftest.run"},
},
```


Broken, but wanted entrypoint of projB:

```
entry_points = {
    "test":{"projB": "projB.conftest.run"},
},
```

Right now, this messes the entrypoint of the packages up.