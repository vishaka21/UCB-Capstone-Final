### Factors that impact AirBnB rental pricing  
**Shweta Raizada**

#### Executive summary
Despite of USA experience a economic slowdown recently, travel in the US continues to boom year over year. People are traveling in large groups, with families, and for extended period of time, contributing to the popularity of vacation rentals like AirBnB. Unlike hotels, the "home away from home" advantage of AirBnB seems to be attractive to travelers, esp for folks who work remotely.
Prices of AirBnB rentals also have skyrocketed with the demand. When traveling with a group, the cost can sometimes break the bank for travelers.
This analysis is attempting to find the factors that could impact the pricing of such rentals. 
We have found that besides the obvious factors like number of beds and baths, luxuries like presence of a pool or hot tub, parking, private entrace and access to a beach also drive up prices. Travelers can avoid rentals with these attributes (if not pertinent to them) to fit their vacation a budget. Also, interestingly, travelers seeking to stay for more than 3-4 days could specifically look for properties that have a high minimum number of nights listed to get cheaper deals. 

#### Rationale
1.	As families or big groups travels and use AirBnB, it’d be useful to find what characteristics draw higher prices. If those characteristics aren’t important to the travelers, they can skip those rentals and save money. This sort of analysis can be especially useful for families traveling on a budget.
2.	When listing their place, hosts could also use this to gauge what a reasonable price for their listing could be. 

#### Research Question
We focused on answering the questions:
- Are there any some Airbnb characteristics that draw higher prices than others at popular destinations
- Do these characteristics differ by the kind of destination? 

#### Data Sources
Airbnb data for listings containing details of the property like characteristics, descriptions, amenities, location, and prices.
Inside AirBnB is an excellent collaboration that has put together a lot of data on AirBnB rentals with the intent to provide data and advocacy about Airbnb's impact on residential communities. We can source the data from this website. 
http://insideairbnb.com/get-the-data 
We used data from cities (NYC, Los Angeles, Chicago, Seattle), mountain towns (Asheville, Bozeman, Denver) and coastal cities (Hawaii, San Diego, Pacific Grove). 

#### Methodology
1.	Exploratory data analysis: Assembled the data, addressed missing values by dropping or impunating them based on the context, addressed outliers for various features where the data seemed unreasonable (e.g. minimum of nights > 365, nightly cost of $99,100 or 50 baths) 
2.	Feature engineering: Parsed amenities data to create categorical variables indicating various attributes of the rental, like, is there a pool? does it offer good views? private parking? etc. To ensure, we aren't taking highly correlated variables into the model, we performed a correlation heatmap analysis and combined a couple of these variables. 
3.	Various Regression algorithms to find contributing factors: Ran Linear Regression, Ridge Regression and Lasso regression models to find an approporaite set of contributing factors. The models gave comparable results and consistent findings in terms of which factors are important. To ensure that our data samples aren't biased when created the models, we performed cross validation on Linear and Ridge models. 

#### Results
Results that were obvious prior to analysis but confirmed through analysis: The number of bed and baths has a high impact on the price of a rental. As you'd imagine, higher the number of beds or baths, higher the price. To note, number of beds has a higher impact than baths.

Results that weren't as obvious and can be used to determine your choice of rental:
1. In general, having a pool or hot tub increases the price of a rental. If the consumer isn't interested in this luxury, they should look for equivalent properties without a pool or hot tub, and save money. This is more prevalant in cities and coastal areas than mountains. 
2. Parking on coastal areas comes with extra $$$. If not an important feature, consumers can skip rentals with parking. Conversely, hosts offering parking should note that it does add value to their rental.
3. Private entrace in cities seems to drive up prices. 
4. Access to a beach or a beach front property adds to a properties nightly rate in coastal areas and in cities. If not desired, skipping this feature can lower the cost of travel.
5. For travelers who are looking to vacation for a longer period of time (e.g. > 7), may want to specifically look into properties that have a minimum number of nights. Such a restrictions seems to be driving down the price of rentals and can save $$$. An equivalent property without a minimum number of nights may cost more.

#### Next steps
1. We did not find a lot of factors specifically for cities. A reasonable next step for this analysis could be to focus on data from cities and find contributing factors. We could use a mix of cities from various regions of the US. 
2. If we formalize this model, it can be used as a tool for consumers to compare the host price with the price listed by the hosts. Often, travelers aren't sure if the steep prices are well worth it or typically of the area. 

#### Outline of project
https://github.com/vishaka21/UCB-Capstone-Final/blob/main/Untitled.ipynb

Segments in the notebook:
1. Data assembly
2. Data preparation
3. Data visualization
4. Feature Engineering
5. Modeling:
    a. Linear Regression
    b. Ridge Regression
    c. Lasso Regression
    d. Cross validation for Linear and Ridge regressions
    e. Linear regression for a subset of data for each location type

##### Contact and Further Information
Shweta Raizada
Engineering Manager
412-708-7343

[def]: image-1.png