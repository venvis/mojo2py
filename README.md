  <div class="examples" id="examples" display="flex" flex-direction="row" align="center">
<h2 align="center"> Mojo2py  <img src="https://img.shields.io/badge/Mojo2py-v1.0-orange"></img></h2>
   
  </div>
<br>
  <div class="examples" id="examples" display="flex"  align="center">
<img align="center" src="mojo2py.png" height="70" width="70"></img>

  </div>
<br>
  <div class="examples" id="examples" display="flex"  align="center">
<p>A python package which converts a mojo file (.mojo or .🔥) into a python file.</p>
  </div>

### Installation  using pip
```shell
pip install mojo2py
```
### Or clone the repo
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

