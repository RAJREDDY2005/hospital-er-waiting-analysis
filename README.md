# Hospital ER Analysis
analysis 0f ER patient wait times,satisfaction,and admissions using Phython and power BI
#Objective

the analysis performed didn't identify statistically significant evidence that describes gender, race , age or department refferal is associated with patient waiting time. as the correlation between patient wait time and patient satisfaction score is ~0 so doesn't show much variation. but if we go through statistical analysi we can see increase in patient waiting time lowers the satisfaction.

And in time series analysis it is observed that most patients are admitted on the month of august(1300++). while in weekdays most patients admitted on saturdays(1700++), and ER is busiest in hours of 11:00 pm.

## Dataset
-~9,200 patient (vists 2023 to 2024)
-Colomns:admission data,age,gender,race,department,referral,admission flag,satisfaction score,wait time

## Tools
Python (pandas,seaborn,scipy,scikit-learn),Power BI,DAX


## Key Finding
-Neurology Department  has the longest average wait(36.8 min)
-Satisfaction falls as waits exceed 35.22 min (Spearman p=-0.00789446359548945)
-Peak visits:<saturday>,<23:00>,<August>
-wait-time disparites by gender/race:<P values : MannwhitneyuResult(statistic=np.float64(10433842.5), pvalue=np.float64(0.33799767285149207)),
 KruskalResult(statistic=np.float64(3.2644493126078173), pvalue=np.float64(0.774998237412856)),
F_onewayResult(statistic=np.float64(0.5485829010796465), pvalue=np.float64(0.7714545724644724))
> 

-this doesn't provide enough evidence not to reject null hypothesis

A random Forest predicting admission reached 51% accuracy(baseline 50%),so the available features carry little predictive signal.

## Dashboard
![Time series analysis](<Screenshot 2026-10-20 223136.png>)


## How to Run
```bash
git clone https://github.com/RAJREDDY2005/hospital-er-waiting-analysis.git
cd hospital-er-analysis
pip install -r requirements.txt
jupiter notebook notebooks/er_analysis.ipynb
