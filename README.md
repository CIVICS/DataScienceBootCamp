# DataScienceBootCamp
For Civic Hacking project quick start onboarding

## Python Quick Start

### Anaconda

* Why Anaconda?  Other tools are just as good but this is one that we like and want to try for this bootcamp.  This is a convenient way to get the basic environment set up to install the key libraries and it creates a launcher.  

### JuPyter

* It is a "REPL" (Read, Eval, Print, Loop) notebook for doing interactive development. 

* Importantly, JuPyter also stores a record of the steps you took and each version of your scripts and such.  This is key for "reproducible" research and for the scientific in general.  

### Python NumPy

### Pandas 

* Panda is like "R" in that it creates "data frames" but it's build on NumPy

# Getting Started

Start with some import statements.  Let's bring the code from other packages into the current script.  We can then access the routines, functions, etc from other libaries.  Start with this:

```python
from datetime import datetime
import matplotlib
import matplotlib.pylab as plt
import pandas as pd
import numpy as np
```

* Now let's get some data!  Start with: https://data.somervillema.gov/resource/q3yh-mp87.json 

* Try: pd.read and hit the tab so you can see what you can do (eg with sql or json, etc)

* Run: 
'''python
df=pd.read_json("https://data.somervillema.gov/resource/q3yh-mp87.json")
df
'''
* While an astrix appears between the brackets in the row to the left, the program is working hard!  Give it some time to ingest and process the data at the URL.  

* There is no standard data format in JSON, so we need to get that data into a format we can use to process it.  To wrangle the date format, do this:

```python
permits[["applicationdate"]] = pd.to_datetime(permits["applicationdate"])
permits[["expirationdate"]] = pd.to_datetime(permits["expirationdate"])
```
