# SENTIMENT ANALYSIS
This is a practice problem on TensorFlow 2.0 Sequential Models Deep Learning on NLP, using the very famous Movie Reviews data for Sentiment Analysis for fun.

# MODEL
The model itself has been saved in my_model.h5 so that you would not need to re-train it and you can only just import it. Otherwise, re-running this code should take 15-30 min.

embedding  = \"https://tfhub.dev/google/tf2-preview/gnews-swivel-20dim/1\" <br />
Epochs     = 20                                                            <br />
optimizer  = adam,                                                         <br />
loss       ='binary_crossentropy'                                          <br />
metrics    = accuracy                                                      <br />

# OUTPUT
The output of the classification model is included in this google drive link, feel free to download it and look at the model output. 
https://drive.google.com/open?id=1FG_3MRtqqW2v45vUXN6mJEZCbMNs73F9

# ENVIRONMENT
## Conda Environment
For step by step insutructions on setting up the environment, please refer to the video in the following link.
https://drive.google.com/open?id=14ZDVDUIVT8WA9pkxIPgF4HXQbO8Mlnv8

The minimum prequisite of course is to have anaconda installed on your machine. I personally have it for Python 3.6

The general steps are : 
1- conda create -n tensorflow_env tensorflow
2- Go to Anaconda Navigator / Environments to find the environment called tensorflow_env
3- Go to uninstalled packed and install tensorflow_hub , tensorflow_datasets
4- Go to Home while being on the tensorflow_env environment and install jupyterlab
5- launch jupyter notebook 

## PYTHON VERSION
### Python 2.7 - Tensorflow 2.0.0 (One currentley using)
Currentley in conda environments Tensorflow is only compatiable with python 2.7 and when creating one, it by default install the 2.7 version. 

### Python 3.6 - Tensorflow 1.0 (didn't try it)
UnsatisfiableError: The following specifications were found to be in conflict:
  - python 3.5*                     <br />
  - tensorflow 2.0* -> python 2.7.* <br />
Use "conda info <package>" to see the dependencies for each package. 

### Python 3.6 - Tensorflow 2.0.0 (didn't try it)
conda create -n tensorflow_env3 tensorflow python>=3.5 <br />
pip install --upgrade pip                              <br />
pip install tensorflow==2.0.0                          <br />

## HARDWARE SPEC
Model Identifier:	MacBookPro11,1
Processor Name:	Intel Core i5
Processor Speed:	2.4 GHz
Number of Processors:	1
Total Number of Cores:	2
L2 Cache (per Core):	256 KB
L3 Cache:	3 MB
Hyper-Threading Technology:	Enabled
Memory:	8 GB
Boot ROM Version:	156.0.0.0.0

# ANALYSIS

## Visual Analysis
https://drive.google.com/open?id=1oH0pCjV5z2kDrj7Lmvj3kziUmQF_CbaZm3ljeJhFzOQ

## Qualitative Analysis
The analysis is included in the links below but here are some examples of Sentiment Scoring on Extreme Cases: 

- Drop what your doing right now and go check it out, you will not regret it trust me it's one of the best T.V shows ever!
- The whole thing looks very cheap & the acting is pretty bad. Predator Island is crap, I'm sorry but that's the way it is & I just fail to see what anyone would get out of it. In my humble opinion this probably one to avoid.

https://drive.google.com/open?id=1r-eBSDK_qRCu4XgWNBEadZtYujGXoTdxEkmdL0IzFyc

## Quantitative Analysis
Test Data Size               :  25K    <br />
Positive Samples             : 12500   <br />
Negative Samples             : 12500   <br />
Threshold                    :  0.5    <br />
Total True                   :  21581  <br />
Total False                  : 3419    <br />
Total True  Positives        : 10,765      -  86%           of Positive Sentiment  <br />
Total False Positives        : 1,735       - 14%            of Positive Sentiment  <br />
Total True Negatives         : 10,816      - 86.5%          of Negative Sentiment Records  <br />
Total False Negatives        :  1,684      - 13.5%          of Negative Sentiment Records  <br />

Accuracy : TT  / Test Data Size  =  21581   / 25000           = 0.86324  <br />
Precision : TP  / TP + FP        =  10765   / (10765 + 1735)  = 0.8612   <br />
Sensitivity: TP / TP + FN        =   10765 /   (10765 + 1684) = 0.8647   <br />

