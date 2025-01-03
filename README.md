# install enviroement
```shell
bash install.sh
```
## 非slambook环境配置start
### git clone
```shell
cd ~/gym/download/slam
# git clone https://github.com/rmsalinas/DBow3.git
# git clone https://github.com/stevenlovegrove/Pangolin.git
# git clone https://github.com/strasdat/Sophus.git
# git clone https://github.com/ceres-solver/ceres-solver.git
# git clone https://github.com/RainerKuemmerle/g2o.git
# git clone https://github.com/google/googletest.git
```
### Pangolin install
```shell
# https://blog.csdn.net/ainitutu/article/details/107084691
cd Pangolin
mkdir build
cd build
cmake ..
make -j16
make install
```
### Sophus install
```shell
# wget https://gitlab.com/libeigen/eigen/-/archive/3.4.0/eigen-3.4.0.tar.gz
# tar -zxvf eigen-3.4.0.tar.gz
# 修改CMakeLists.txt中的cmake版本和Eigen版本
cd Sophus
mkdir build
cd build
cmake ..
make install
```
### Ceres-solver install

```shell
# easy install
apt install libceres-dev -y
apt-get install libceres-dev -y
# complex install
# https://blog.csdn.net/little_white138/article/details/142443296
apt-get install -y libgoogle-glog-dev libgflags-dev protobuf-compiler libprotobuf-dev
apt-get install  liblapack-dev libsuitesparse-dev libcxsparse3 libgtest-dev -y
cd ~/gym/download/slam
git clone https://github.com/abseil/abseil-cpp.git
cd abseil-cpp
cmake -DBUILD_SHARED_LIBS=ON -L CMakeLists.txt && make -j16
make install
cd ..
wget http://ceres-solver.org/ceres-solver-2.0.0.tar.gz
tar -zxvf ceres-solver-2.0.0.tar.gz
cd ceres-solver
mkdir bd
cd bd
cmake ..
make -j16
make install
```
### G2o install
```shell
cd ~/gym/download/slam
git clone https://github.com/RainerKuemmerle/g2o.git
cd g2o
mkdir build && cd build
cmake ..
make -j16
make install
```