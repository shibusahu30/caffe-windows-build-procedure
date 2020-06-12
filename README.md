# caffe-windows-installation-procedure
11-Jun-2020
[source for buid](https://github.com/shibusahu30/caffe/tree/windows)
# For CPU only
## Requirements
  1. Microsoft Visual Studio 2015
      * Download Visual Studio from [here](https://my.visualstudio.com/Downloads)
      * During installation, you must include following components:
          1. All of Programming Languages -> Visual C++
          2. Windows and Web Development -> Universal Windows App Development Tools -> Tools(1.4.1) and Windows 10 SDK (10.0.14393)
          3. Windows and Web Development -> Windows 8.1 and Windows Phone 8.0/8.1 Tools -> Tools and Windows SDKs 
  2. Anaconda2(64 bit) with Python 3.5
     (I found in someones article to use Anaconda2 not Anaconda3. U can also give a try with Anaconda3 with following procedure.)
      * Download Anaconda2(64 bit) from [here](https://www.anaconda.com/products/individual#Downloads)
      * It's default python version is 2.7, create python3.5 with following command in Anaconda Prompt:
          ```cmd
          :: update conda
          (base) > conda update conda
          :: create environment for python 3.5
          (base) > conda create --name py35 python=3.5
          :: activate 
          (base) > conda activate py35
          :: setup required for caffe
          (py35) > conda config --add channels conda-forge
          (py35) > conda config --add channels willyd
          (py35) > conda install --yes cmake ninja numpy scipy protobuf==3.1.0 six scikit-image pyyaml pydotplus graphviz
          ```
      * Add path to system environment i.e. path\Anaconda2\envs\py35. This path should be added at the top of all other python paths of your system environment.
  3. CMake 3.5 or higher
      * Download CMake from [here](https://cmake.org/download/)
      * Add path of binary file to your system environment i.e. path\cmake-3.17.3-win64-x64\bin
  4. Matlab 2014b from [here](https://in.mathworks.com/downloads/web_downloads)
  5. Git from [here](https://git-scm.com/downloads)
## Configuring and Building Caffe
```cmd
  :: clone the repo
  > git clone https://github.com/BVLC/caffe.git
  :: change dir
  > cd caffe
  :: goto windows branch
  > git checkout windows
  :: Edit any of the options inside build_win.cmd to suit your needs according to my build_win.cmd file
  :: then build
  > scripts\build_win.cmd
```


<img src="https://github.com/shibusahu30/caffe-windows-build-procedure/tree/master/images/im1.png" alt="buid summary" width="900px">


<img src="https://github.com/shibusahu30/caffe-windows-build-procedure/tree/master/images/im2.png" alt="caffe config" width="900px">
