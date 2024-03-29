# earthquake-forecast
Forecasting small scale earthquakes in the vicinity of Israel.
The aim of this project is to forecast magnitudes and locations of a small scale (up to 3.5 on a Richter scale) earthquakes in the vicinity of Israel. At this stage based on earthquake data of Geological Survey for a year 2018.
 Location of small magnitude earthquakes along the Dead Sea Fault (North - South) was also forecasted with SK-learn with Linear Regression and XGBoost algorithms.

Motivation and intro:
 Dead Sea region is an active tectonic transform fault. Large scale Earthquakes occur in that region at approximated frequency of about 1/80 years, While small scale Earthquakes are very frequent - sometimes several of those are recorded a day. When Earthquake occurs in tectonically active region it changes the underground stored stresses distribution along the fault (enlarges or releases those stresses at different locations) and thus influences future probability of earthquake occurrence and location probabilities along the fault line.
 Even though it seems to be impossible to predict the next large scale earthquake with the limited information and data available (especially considering the fact that all the info is about small scale earthquakes), it can be possible for an ML algorithms to detect a pattern in small scale magnitude earthquakes and forecast the location of their occurrence over time.

Location of 2018 earthquakes is visualized on the map (with folium package)
![image](https://user-images.githubusercontent.com/101993270/181304040-afa5ce69-1c1a-433c-b110-6ede7cd0dee2.png)

Forecast of Earthquake location along North - South Fault line with SciKit-learn Linear regression and XGBoost:

the errors (RMSE) for train and test sets that were achieved with Linear Regression (shown below) are:
![image](https://user-images.githubusercontent.com/101993270/213099563-e62dff67-1af4-477e-a743-6040996d4b7b.png)

In this region error of 0.1 degree along N-S axis is approximate to 10km. So, RMSE of 0.688 is almost 70 km range, which is a considerable error of course. But keeping on mind that the data in that dataset is spread along approximately 400 km along the Dead Sea fault we may conclude that a prediction with +/-70km still have some predictive validity.

![image](https://user-images.githubusercontent.com/101993270/213099104-ad101888-2403-43dd-ad75-84e05ec3e59d.png)


Forecast of Earthquake magnitude with Pytorch NeuralProphet
![image](https://user-images.githubusercontent.com/101993270/159774480-e60a0b4f-bc10-4c6e-b42a-126e338e0d87.png)

Forecast of Earthquake location (longitude N-S) with Pytorch NeuralProphet
![image](https://user-images.githubusercontent.com/101993270/159774373-fafaae95-d267-4986-8a2f-6b3aec7d4b6c.png)
