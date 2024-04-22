  <div class="examples" id="examples" display="flex" flex-direction="row" align="center">
<h2 align="center"> Mojo2py  <img src="https://img.shields.io/badge/Mojo2py-v1.3-orange"></img><p></p><img src="https://static.pepy.tech/badge/Mojo2py"></img></h2>
   
  </div>
<br>
  <div class="examples" id="examples" display="flex"  align="center">
<img align="center" src="mojo2py.png" height="70" width="70"></img>

  </div>
<br>
  <div class="examples" id="examples" display="flex"  align="center">
<p>A python package which converts a mojo file (.mojo or .🔥) into a python file.</p>
  </div>

### Install using pip
```shell
pip install Mojo2py==1.3
pip3 install Mojo2py==1.3
```
### Clone the repo
```shell
git clone git@github.com:venvis/mojo2py.git
```


#### Initialize a mojo file , for example (example.mojo or example.🔥) :
```mojo

from python import Python 

def matplotlib(x:PythonObject,y:PythonObject):
    var plt=Python.import_module("matplotlib.pyplot")
    var np=Python.import_module("numpy")
    var xval=np.array(x)
    var yval=np.array(y)
    plt.plot(xval,yval)
    plt.show()

fn show() raises:
    try:
        matplotlib([1,2,3,4,5],[6,7,8,9,10])
    except:
        print("Error")

fn main():
    try:
        show()  
    except:
        pass   
```        

#### Create a python file , for example (trial.py) : 

```python
from mojo2py import convert #import the class to convert
file=convert("example.mojo") # or file=convert("example.🔥") , if an error comes give full path to the mojo file
file.final() # Call the final method to generate example.py file from example.mojo
```
#### A file called example.py , with the same name as the mojo file will be created in the same directory and the code is as follows :

```python
import matplotlib.pyplot as plt 
import numpy as np 
 

def matplotlib(x,y):
    xval=np.array(x)
    yval=np.array(y)
    plt.plot(xval,yval)
    plt.show()

def show():
    try:
        matplotlib([1,2,3,4,5],[6,7,8,9,10])
    except:
        print("Error")

def main():
    try:
        show()  
    except:
        pass                  
if __name__=="__main__":
    main()
```

