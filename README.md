# Prediction-of-Business-Success-Failure-Machine-Learning

Setting up a new business is an arduous task. Entrepreneurs often embark in new business ventures with high hopes of success, however research shows that a considerable portion of new firms exit the market soon after entering it (Fritsch et al. 2006). Understanding why this happens is crucial to the economy’s stability and health since business bankruptcy is costly not only to business owners and investors but also to the community as a whole (Pompe and Bilderbeek, 2005).


Previous success/fail model studies have focused on using firms’ specific characteristics to predict whether a business fails or succeeds (Lussier and Halabi, 2010). These characteristics include starting capital, industry and management experience of founder, education and age of founder and many others. Although these factors are important in determining success or failure of a business, Fritsch et al. (2006) argue that a limitation of said studies is that they do not account for the regional dimension. In fact, Fritsch et al. (2006) show that regional factors play an important role in predicting the survival of new businesses. This is in line with the concept of agglomeration economies, according to which cities and clusters of activity boost the productivity of firms located within them (Duranton and Kerr, 2015). Examples of industry clusters the Silicon Valley in the USA for tech firms, or the Sheffield (U.K.) area for cutlery manufacturing (Duranton and Overman, 2004).


The tendency of industries to agglomerate has been greatly studied by economists and geographers, which believe a firm’s localization to be a proxy for innovation and high performance (Claver-Cortès et al. 2015). To continue, Claver-Cortès et al. (2015) explain that a firm’s high performance and innovation rate is given by two factors. The first is the firm’s dynamic capabilities, which refer to organizational skills that allow the business to grow, adapt, create internal and external resources and maintain a competitive advantage despite the changing business environment. The second is the firm’s absorptive capacity, which relates to the ability of the firm to utilise external knowledge to create a competitive advantage over other firms. From this definition it is easy to understand that absorptive capacity comes from a firm’s localisation in dynamic clusters.


Literature on agglomeration suggests that concentration of economic activity generates different outputs for firms. Appold (1995) assumes that profits of firms are positively correlated to the number of firms located near it. To support this, Fritsch et al. (2006) affirms that agglomeration could be beneficial due to a firm’s proximity to research institutions such as universities, to large pools of customers and other companies in the same industry so to facilitate knowledge spillovers. More recent studies found however, that agglomeration can also have negative effects on profits because of higher competition (Arikan and Schilling, 2010). Regarding competition, Fritsch et al. (2006) argue that intensity of competition affects survival chances of a firm suggesting that competition is beneficial until it reaches a certain threshold after which it becomes a negative factor because of too much competition for locations, employees, resources, customers and more. The authors also mention unemployment rate to be relevant in predicting firms’ survival. More specifically, since high unemployment could stand for low growth rate of a region, which might affect a firm’s performance negatively or positively. Second, high unemployment could also mean more availability of labour and should contribute to the success of a firm and last, high unemployment could lead to the creation of new businesses by unemployed people and also this could affect the probability of success or failure of a firm.


Given the background illustrated above, I this report aims at creating a machine learning model able to predict success or failure of new tech businesses in England. The factors that will be taken into consideration are:
* Regional characteristics including: o Population density
* Density of firm in the same sector o Unemployment rate
* Availability of research institutions
* Firm specific characteristics (limited to data availability)

The methods used to answer this question are logistic regression and random forest algorithm.

## The Data

The data used to create the machine learning model comes from different sources. The main data set was retrieved from the Consumer Data Research Centre and it contains information about all public and private businesses in England as of 2017.

Because the business data set contains information about the location of the company, I was able to link this data set with demographic information relating to the geographical area the company is located into. The U.K. Data Service allows users to freely download aggregate data of the latest census at various geographical levels. For this research, I have decided to download census data at ward level. England is composed of 7,678 wards and this allowed me to get precise information about the geographical position of a company. Following the example of Fritsch et al. (2006), I decided to attach to the original dataset geographical data regarding:
* Population density of the ward where the company is located
* Economic activity of residents. Economic activity related to whether or not a person (16 or
over) is working or looking for work during the week before census. This indicator provides a measure of whether or not a person was an active participant in the labour market (UK Data Service, n.d.)
* Unemployment. More specifically, the portion of the population who is actively participating in the labour market but was unemployed the week before census.
* Education level. More specifically, the portion of the economically active population with a higher education degree.
* Research institutions. University play a fundamental role in the UK economy. They support economic growth and help overcome weaknesses in the UK economy such as decreasing labour productivity, low R&D investment and skills shortage (Allas, 2014). For this reason, I decided to include data regarding the presence of universities in the city the company is located into.
