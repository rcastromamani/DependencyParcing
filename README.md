# DependencyParcing

#### Compiling LSTM parser
#### ---------------------

$ sudo apt-get install g++-5
$ sudo apt-get install mercurial 
$ cd /media/sf_RCastroq/Instaladores/DeepLearning_DepedencyParsing/
$ hg clone https://bitbucket.org/eigen/eigen
$ mkdir /home/richard/Documents/build_eigen
$ cd /home/richard/Documents/build_eigen
$ cmake /media/sf_RCastroq/Instaladores/DeepLearning_DepedencyParsing/eigen
$ make
$ sudo make install

$ cd /media/sf_RCastroq/Instaladores/DeepLearning_DepedencyParsing/lstm-parser/
$ git clone https://github.com/clab/lstm-parser.git
$ cd lstm-parser
$ rm -rf cnn
$ git clone https://github.com/clab/cnn.git
$ mkdir build
$ cd build
$ export CC=/usr/bin/gcc-5
$ export CXX=/usr/bin/g++-5
$ cmake .. -DEIGEN3_INCLUDE_DIR=/usr/local/include/eigen3
$ make -j2

