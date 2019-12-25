# Industrial-Power-Demand-Dataset
The practical real-time power demand datasets named Industrial-Power-Demand-Dataset(IPDD) is collected form a steel plant, which consists of three-phase electric current, three-phase active power and three-phase demand active power of the entire plant, and the interval of this collected raw data is 30 seconds. The structure of IPDD as follows:
```
├── testset
└── trainingset
```
And the original attributes in the dataset as shown in the table below：

there are two observations about the power demand. Present power demand T_DEM, the value for the last completed interval, which is used to predict and compare with the maximum demand limit. Recent power demand S_DEM, which is the real time value measured by the field data acquisition meters, and which represents the trend in the near future.
###### trainingset
This is the raw data collected from May 4 to July 15, 2018. According to that the step size of the sliding time block for power demand is set to 1 minute, when using the trainingset to train model for Ultra-short-term industrial power demand forecasting, you could to sample the records of trainingset at 1 minute intervals.
###### testset
Ten testing datasets, which are randomly selected from the raw data collected from July 15 to August 9, 2018, not included in the training dataset. During the forecasting, you could to select the first m time-steps of the series at 1 minute intervals and then predict the power demand of the next n time-steps.
