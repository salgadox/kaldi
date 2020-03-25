
# Training Acoustic Models in Kaldi 

## Usefull information 
### What is kaldi? 
- A state-of-the-art automatic speech recognition toolkit. 
Please refr to kaldi website for further information. 

### how to install kaldi? 
- refere to the kaldi-installation.md   

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
- Create the following directories: 
```
mkdir exp conf data
mkdir data/train data/lang data/local
mkdir data/local/lang
```
#### data/train File: 

will contain informartion about the audio files

  - text: transcript of the corpus, utterance by utterance (id_utterance WORD1 WORD2 ... WORDN)
    - Example text file:
      AA-test-F-S-AAS820006-00000 la formation professionnelle est un enjeu majeur tant du point de vue de nos performances économiques que du point de vue des idéaux de justice sociale
 
 -segment:  
