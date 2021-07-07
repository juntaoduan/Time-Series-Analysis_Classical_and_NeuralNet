# Time Series Analysis (TSA) with classical and deep learning in Python 
Explore and compare classical time series models, such as Arima, with deep learning models such as Transformers.

## Conclusion: Language can be memorized but time series can not!
* From this experiment, we can confirm that Neural network in general does not outperform the classical wisdom of decoposing time series. In the following experiment, one consistently see Arima outperform Neural networks. So what is going on?
* 1. Why does deep learning fail to help us? There are several reasons.
    * The bottom line is learning language is very different from learning to predict time series. Time series data come naturally from dynamics of a certain real world system and it is usually continuous and volatile which made it is hard to capture the pattern completely. On the other hand, language can be learned completely and characterized 100% by human. With minimal degradation, we encoded language with letters and symbols so we can communicate long range both in time and space. Due to the very large capacity of a transformer-type neural network model, it can simply memorize this encoding and make 'human-natural' predications of language. While time series does not have the luxuary of 'memoriz-ability' and usualy exhibits chaotic behavior.
    * Continuous vs discrete. Language naturally is discrete and can be easily embeded into a low dimensional space. It is possible to memorize the seperation of discrete signals. On the other hand, continous time series signal is more adapted to a decomposition type modeling such as Fourier and wavelet transformations.
    * Data scale:  i.i.d large squences (almost infinitely many squences) vs weak dependent seuence(one squence). Language training dataset is enoumous (considering [common crawl](https://github.com/juntaoduan/Time-Series-Analysis_Classical_and_NeuralNet/edit/main/Readme.md) have hundreds of TB data) naturally repeat itself with specific lingustic structures and patterns. Even though each sentence is sequentially produced but the training data have i.i.d. of thes sentences.  On the other hand, time series sequence has only one unique observed sample from a stochastic system.
* 2. Is calssical statistical method the only way to model time series?
    * The answer is False. When many time series put together, dataset become large and complex, classical method is too simple and naive which losses much of the details. Then there is an alternative solution that is to handcraft features and uses tree-type of structure discovering models, for example Gradient Boosting Tree.

   
## Table of contents

* [General info](#general-info)
* [Results](#results)
* [Methods and Tools](#methods-and-tools)
* [Code Examples](#code-examples)
* [Status](#status)
* [Contact](#contact)
* [Reference](#reference)

## General info

The project is meant to compare classical Time Series models, such as ARIMA method with the recently emerged transformer model.

Major steps involved in classical time series analysis were as follow :                                 
* STEP: 1 - Data Cleaning and Analysis
* STEP: 2 - Checking Stationarity (ADF Test) 
* STEP: 3 - Transformation, Differencing  
* STEP: 4 - Finding ACF and PACF
* STEP: 5 - ARIMA, SARIMAX modeling and testing

Major steps involved in transformer: 
* STEP: 1 - Create cusomized transformer architecture for time series
* STEP: 2 - Design data class and create data in batch
* STEP: 3 - Build transformer 
* STEP: 4 - Train and fine-tune parameters on the data
* STEP: 5 - Testing and saving model

** Compare the methods on single variable and multiple variables time series data

## Results

![Arima](./ET_Arima.png 'ET_Arima')
![LSTM](./ET_LSTM.png 'ET_LSTM')
![Transformer](./ET_Transformer.png 'ET_Transformer')
![Transformer with linear head](./ET_Transformer_LH.png 'ET_Transformer with linear head')


## Methods and Tools
* Python 
* Pytorch
* Statsmodels
* ARIMA, SARIMAX
* Transformer
* Dickey-Fuller Test
* ACF and PACF


## Code Examples

````


````

## Status
Project is: _Ongoing_.

## Contact
Please feel free to reach me at 
<a href="mailto:jt.duan@gatech.edu">email</a> 


## Reference
* [AileenNielsen](https://github.com/AileenNielsen/TimeSeriesAnalysisWithPython)
* [Informer2020](https://github.com/zhouhaoyi/Informer2020)
* [Manishms18](https://github.com/Manishms18/Air-Passengers-Time-Series-Analysis) 
* [TorchTransfomer](https://github.com/pytorch/pytorch/blob/master/torch/nn/modules/transformer.py)
