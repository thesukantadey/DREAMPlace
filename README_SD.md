```DREAMPlace``` is successfully executing (without docker) from my install directory, which is ```/home/sukanta/install```, this should be specified during cmake your_install_path.

OS used Ubuntu 20.04 LTS (in virtual box).
For successful installation:

Clone it
```git clone --recursive https://github.com/limbo018/DREAMPlace.git```

Check requirements and install everything
```pip install -r requirements.txt```

Installation:
```mkdir build
cd build
cmake .. -DCMAKE_INSTALL_PREFIX=/home/sukanta/install/ -DPYTHON_EXECUTABLE=$(which python)
make
make install
```


After that, dreamplace will be installed at ```/home/sukanta/install``` <br/>
Go to ```/home/sukanta/install/``` <br/>
Download benchmarks by following command ```python benchmarks/ispd2005_2015.py```<br/>
Disable GPU by changing in json files<br/>
Execute ```python dreamplace/Placer.py test/ispd2005/adaptec1.json```<br/>
Test ```python unittest/ops/hpwl_unittest.py```<br/>


Your torch and torchvision should be installed into root directory. I was getting error because torch was not available in the root.

Please follow the following if cmake error occurs.
https://github.com/limbo018/DREAMPlace/issues/48#issuecomment-973262778
