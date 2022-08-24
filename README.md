## Analyzing Forest Fire Data

Forest fires can create ecological problems and endanger human lives and property. Understanding when they occur and what causes them is important for managing them. The data we’ll be working on within this guided project is associated with a scientific research paper on predicting the occurrence of forest fires in Portugal using modeling techniques.
Here are descriptions of the variables in the data set and the range of values for each taken from the paper:
* `X`: X-axis spatial coordinate within the Montesinho park map: 1 to 9
* `Y`: Y-axis spatial coordinate within the Montesinho park map: 2 to 9
* `month`: Month of the year: ‘jan’ to ‘dec’
* `day`: Day of the week: ‘mon’ to ‘sun’
* `FFMC`: Fine Fuel Moisture Code index from the FWI system: 18.7 to 96.20
* `DMC`: Duff Moisture Code index from the FWI system: 1.1 to 291.3
* `DC`: Drought Code index from the FWI system: 7.9 to 860.6
* `ISI`: Initial Spread Index from the FWI system: 0.0 to 56.10
* `temp`: Temperature in Celsius degrees: 2.2 to 33.30
* `RH`: Relative humidity in percentage: 15.0 to 100
* `wind`: Wind speed in km/h: 0.40 to 9.40
* `rain`: Outside rain in mm/m2 : 0.0 to 6.4
* `area`: The burned area of the forest (in ha): 0.00 to 1090.84
 
The goal of this work is to answer questions such as
* *Which months do forest fires happen the most?*
* *Which days of the week do forest fires happen the most?*
* *Any of the variables have values that stand out during August and September, which we’ve previously confirmed sees a lot of fires?*
 
![](https://github.com/rennnas/guided-project-r-2/blob/main/guided-project-2-imagem1.png
![](https://github.com/rennnas/guided-project-r-2/blob/main/guided-project-2-imagem2.png)
![](https://github.com/rennnas/guided-project-r-2/blob/main/guided-project-2-imagem3.png)
![](https://github.com/rennnas/guided-project-r-2/blob/main/guided-project-2-imagem4.png)

Looking at the data immediately though, there is no variable that describes just “severity”. Many times in analysis, we’ll be interested in a variable, but simply won’t have the data for it. In these cases, we often have to look at proxies, or a kind of “representation” of severity. In this data set, the area variable contains data on the number of hectares of forest that burned during the forest fire. We’ll use this variable as an indicator of the severity of the fire. The idea behind using area as a proxy is that worse fires will result in a larger burned area. Of course, this won’t be true in all cases, but it is a reasonable assumption to make.
