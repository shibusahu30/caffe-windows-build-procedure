# caffe-windows-build-procedure

# For CPU only
## Requirements
  1. Microsoft Visual Studio 2015
  2. Anaconda2 with Python 3.5
  3. CMake 3.5 or higher
  4. Matlab 2014b
  5. Git
## Configuring and Building Caffe
```cmd
  > git clone https://github.com/BVLC/caffe.git
  > cd caffe
  > git checkout windows
  :: Edit any of the options inside build_win.cmd to suit your needs according to my build_win.cmd file
  > scripts\build_win.cmd
```
