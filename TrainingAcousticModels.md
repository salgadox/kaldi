
# Training Acoustic Models in Kaldi 

## Usefull information 
### What is kaldi? 
- A state-of-the-art automatic speech recognition toolkit. 
Please refr to kaldi website for further information. 

### how to install kaldi? 
- refere to the README.md  

### Understanding Kaldi's directory structure: 
Top-level directories : cmake           COPYING  egs      misc       scripts  tools
CMakeLists.txt  docker   INSTALL  README.md  src      windows

- egs : examples, contains examples rrecipes that can be used as a template for future projects. 
- src : source, contains most of the source code for programs that the training recipies call. 


## Preparing directories 

- Create a directory for your training data and your model
```
cd kaldi/egs 
mkdir corpus
```
-Choose your template, for example: wsj. 

- Copy of wsjs' path.sh script and make sure that the KALDI-PATH root is correct 
```
cd corpus
cp .../wsj/s5/path.sh 
```
- Make a link to src 
```
ln -s ../../src . 
```
- Make soft links to the following directories: steps, s5/utils and 
```
ln -s ../wsj/s5/steps .
ln -s ../wsj/s5/utils .
```
- Create 

