SystemBoost
===========

Jamfile exposing the system installed Boost to Boost-Build

Features
--------

- Auto detect *-mt* suffix
- Expose target for most libraries
- Expose dummy target *headers* to be compatible with using boost sources
- Works with MSVC (Libraries must be in PATH)

Usage
-----

Alias it with your Jamroot:
```
use-project /boost : libs/SystemBoost ;
```

Use it in your target:
```
exe MyApp
    : MyApp.cpp
      /boost//program_options
      /boost//date_time
```
