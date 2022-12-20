


#### [N-BEATS: NEURAL BASIS EXPANSION ANALYSIS FOR INTERPRETABLE TIME SERIES FORECASTING](https://arxiv.org/pdf/1905.10437.pdf)

> *Conference:  ICLR 2020 | Authors: Boris N. Oreshkin, Dmitri Carpov, Nicolas Chapados and Yoshua Bengio*  

> **Brief background:** 
    Makridakis et al. (2018b) argued that "hybrid approaches and combinations of method are the way forward for improving the forecasting accuracy and making 
    forecasting more valuable". In this work, authors challenge this conclusion and propose a pure DL architecture in the context of time series forecasting. 
    They specifically look into univariate time series forecasting problem and show considerable improvements over state of the art (at that time) hybrid approaches.

> **Key idea:** 
    The basic building block of their architecture is a double residual stack. In traditional residual blocks, we add input of some of the previous layers to the output of current layer, and pass the combined result to the next layer. This helps in better training of deep architectures, by allowing gradients to directly flow through several layers (if I have layer 1 output going at layer 10, their gradients are directly connected with residual connection, while without residual connection layer 1 is connected to layer 10 with long path of 10->9->8 ... ->1. The authors of this paper build upon the idea of residuals, specifically introducing "double residual branching". Each layer of their model has 1) predicted projection of past data ($\hat{x_l}) and 2) future foreast ($\hat{y_l}$). The residuals connections also run through these two branches: 1) past projection branch where they take the difference of layer input (${x_l}) with layer output (\hat$x_l$), and 2) future forecast branch where they add outputs ($\hat{y_l}$) from all layers in a stack. Multiple such stacks are trained and combined to generate a final prediction, as shown in the figure below. One more key contribution of authors is combining the output components ($\hat{y_l}$) in a fashion such that it can be broken down into trend and seasonality components by introducing monotonicity and periodicity in stack level outputs.       
    

> **One result worth mentioning:** 

    3% over M4 competetion winner on Kaggle with DL/TS hybrid. (althought I didn't )
    

> Model Architecture            | Comparisons of statistical vs hybrid vs N-BEATS on M4 competetion data
> :-------------------------:|:-------------------------:
> <img src="images/nbeats.png" width="600"/>  |  <img src="images/nbeats-results.png" width="600"/>



