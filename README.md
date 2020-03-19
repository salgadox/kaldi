# Install Kaldi


## Kaldi information: 
Kaldi official page: http://kaldi-asr.org/
Kaldi official github: https://github.com/kaldi-asr/kaldi


## Getting Started
These instructions will help install kaldi on a conda environment. 
Make sure you've got miniconda installed (or conda if you've got he space). 

First, you must clone kaldi's repertory:
```
git clone https://github.com/kaldi-asr/kaldi.git
```

 and create a conda environment: 

```
conda create -n kaldi -c conda-forge python=3.7 
conda activate kaldi
```


## Installing
following the [INSTALL instruction](https://github.com/kaldi-asr/kaldi/blob/master/INSTALL)
Steps:   
- **Step 1**
    - go to tools/  and follow INSTALL instructions there.

- **Step 2**
    - go to src/ and follow INSTALL instructions there.


### Step 1 
```
cd tools/
./extras/check_dependencies.sh 
```

In order to not install anything directly on the system use conda to install the dependencies inside your environment

```
conda install -c conda-forge automake autoconf sox
conda install -c conda-forge libtool 
```
Two dependencies wont be avaiable on conda. 
1) subversion 
2) intel mkl 

For subversion ask you administration to install it or use sudo apt install subversion (if you have the rights)

For inter mkl : 
```
conda install -c conda-forge openblas
```

Check that every dependency is already installed and if so do 'make'
```
./extras/check_dependencies.sh 
make
```
### Step 2 

Change directory to src  
```
cd ../src
```
and following the [step2 instructions](https://github.com/kaldi-asr/kaldi/blob/master/src/INSTALL)
do

```
./extras/install_openblas.sh
./configure --shared --mathlib=OPENBLAS
make -j clean depend; make -j 8 
```

Finally you can add Kaldi to your $PATH 
