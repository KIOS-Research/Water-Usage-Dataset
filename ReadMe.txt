CITATION REQUEST
================
If you have found this dataset or parts of it useful, please cite our work as follows:

P. Pavlou, S. Filippou, S. Solonos, S. G. Vrachimis, K. Malialis, D. G. Eliades, T. Theocharides, M. M. Polycarpou. Monitoring domestic water consumption: A comparative study of model-based and data-driven end-use disaggregation methods. Journal of Hydroinformatics.



DATASET DESCRIPTION
===================
This dataset concerns the monitoring of water usage of different household appliances. Informing consumers about it has been shown to have an impact on their behavior toward drinking water conservation. The data were created using the STochastic Residential water End-use Model (STREaM) (Cominola et al., 2018), a modelling software developed that generates synthetic time series data of a household.


Resolution = 10s
Number of Appliances= 5
Active Appliances: standard toilet, standard shower, standard faucet, high-efficiency clothes washer and standard dishwasher
Household: 2-person
Dataset Duration: Training dataset - 90 days, Validation dataset - 45 days, Testing dataset - 45 days

Train Files:
- Trainset.csv: CSV file containing the 6 columns of data. The total consuption and 5 columns indicating the consumption of the appliance/s that is/are active.


Validation Files:
- Validationset.csv: CSV file containing the 6 columns of data. The total consuption and 5 columns indicating the consumption of the appliance/s that is/are active.


Test Files:
- Testset.csv: CSV file containing the 6 columns of data. The total consuption and 5 columns indicating the consumption of the appliance/s that is/are active.



BASELINE MODEL PERFORMANCE
==========================
In the aforementioned journal article, we have proposed two different approach to address the problem, a model-based and a learning-based. The first method is model-based (MB) and uses a combination of Dynamic Time Wrapping and statistical bounds to analyze four water end-use characteristics. The second learning-based (LB) method is data-driven and formulates the problem as a time-series classification problem without relying on a priori identification of events. Initially four algorithms are considered for the LB method: Support Vector Machine (SVM), Random Forest (RF), Extreme Gradient Boosting (XGBoost) and Multilayer Perception (MLP) with the last one been the most accurate. 

	        MLP	XGBoost	RF	SVM
Accuracy (%)	98.89	98.78	96.51	98.34
F1-Micro (%)	71.73	71.98	55.75	65.29

The results from the MB and the selected LB approach are presented below:

		Model Performance
	Precision (%)	F1-score (%)	Cohen’s Kappa (%)	ROC-AUC (%)
LB	77.61	        71.73	        71.62	                83.36
MB	71.88	        71.04	        70.82	                84.93


LICENCE
=======
TODO
