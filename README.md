# Description

This is a kaggle contest I participated in for my STAT 441 (Classification) course at UW. We used a dataset to predict answers to the question: "On a scale of 1 to 10, how right or poor do you think you are right now (1 being very poor and 10 being very rich". We got second place out of all participants in our class (total of 40 teams).

![Alt text](/imgs/kaggle-constest-details.png)

Each observation is a survey response of one person. Each person is identified by 3 codes: "psu" (Primary Sampling Unit), "hh" (Household), and "idcode". 

We were evaluated on how accurate our response for the question was based on the training dataset. After data cleaning and transformation, we were left with 5334 observations in total, in which we employed 5-fold Cross Validation to improve our model robustness.


## Evaluation metric
- Used Multi-class Logarithmic Loss:

$$
MLC = -\frac{1}{n} \sum^N_{i=1} \sum^M_{j=1} y_{ij} \log(p_ij)
$$

where $y_{ij}$ is an indicator to whether sample $i$ belongs to class $j$, and $p_{ij}$ is the probability predicted by the model that sample $i$ belongs to class $j$.
