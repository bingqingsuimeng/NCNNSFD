![](https://raw.githubusercontent.com/Tencent/ncnn/master/images/256-ncnn.png)
# ncnn

[![License](https://img.shields.io/badge/license-BSD--3--Clause-blue.svg)](https://raw.githubusercontent.com/Tencent/ncnn/master/LICENSE.txt) 
[![Build Status](https://travis-ci.org/Tencent/ncnn.svg?branch=master)](https://travis-ci.org/Tencent/ncnn)


ncnn is a high-performance neural network inference computing framework optimized for mobile platforms. ncnn is deeply considerate about deployment and uses on mobile phones from the beginning of design. ncnn does not have third party dependencies, it is cross-platform, and runs faster than all known open source frameworks on mobile phone cpu. Developers can easily deploy deep learning algorithm models to the mobile platform by using efficient ncnn implementation, create intelligent APPs, and bring the artificial intelligence to your fingertips. ncnn is currently being used in many Tencent applications, such as QQ, Qzone, WeChat, Pitu and so on.

---

### Compile
[how to build ncnn library](https://github.com/Tencent/ncnn/wiki/how-to-build)

[how to use ncnn with alexnet](https://github.com/Tencent/ncnn/wiki/how-to-use-ncnn-with-alexnet)

### How To Test SFD 

Follow these steps after you build the library using above compile instructions.

#### Test ncnn-sfd inference performance

You only need .param files in ncnn format to test inference performance. 
Copy all the param files from NCNNSFD/benchmark/ to NCNNSFD/build/benchmark/
```
$ cd build/benchmark/
$ ./benchcnn 8 4 0
```
---Output---
![](ncnnsfd/nviso_benchncnn_example.png)

#### Test SFD image/webcam face detection

Copy .jpg images from NCNNSFD/ncnnsfd/ to NCNNSFD/build/ncnnsfd/.
Copy .param and .bin files from NCNNSFD/ncnnsfd/ to NCNNSFD/build/ncnnsfd/.

1. Test in single image. 
```
$ cd NCNN/build/ncnnsfd/
$ ./mobilenetsfd_image 79378097.jpg NVISO-A7.param NVISO-A7.bin
```
---Output---
![](ncnnsfd/nviso_imagetest_example.jpg)

2. Test in webcam stream.
```
$ cd NCNN/build/ncnnsfd/
$ ./mobilenetsfd_webcam 0 NVISO-A7.param NVISO-A7.bin
```
---Output---
...

### License

BSD 3 Clause

