##### This is a modified MNN library by Alibaba that is compatible to run inference on Nvidia Jetson Nano. Convert ONNX model to MNN model on desktop(x86) and run inference on jetson nano, code is cross compatible.

### Installation

```sh
cd MNN/
sudo apt-get install graphviz libprotobuf-dev protobuf-compiler
./schema/generate.sh
mkdir build
cd build
cmake -DCMAKE_SYSTEM_NAME=Linux -DCMAKE_SYSTEM_VERSION=1 -DCMAKE_SYSTEM_PROCESSOR=aarch64 -DCMAKE_BUILD_TYPE=Release -DMNN_BUILD_CONVERTER=true -DMNN_BUILD_DEMO=ON -DMNN_OPENMP=ON .. && make -j4
sudo make install
cd ..
cd pymnn/pip_package/
sudo python3 setup.py install
sudo ldconfig
```
