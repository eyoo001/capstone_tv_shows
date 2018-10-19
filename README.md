# Predicting Television Show Success Using IMDB
_By Eric Yoo_


### The Opener

Mainstream television networks have traditionally been seen as an having made its decisions based moreso on bean counters than on baseless gambles - this means that the industry should be the perfect place to try and deploy effective, production-ready machine learning. There is certain to be a mountain of data that is being collected by marketing and government agencies about audiences and viewership that are not being utilized to its fullest. On the other hand, Hollywood's reluctance to adapt to new, upcoming technologies is what has led to the networks losing significant amounts of their audiences from television shows to streaming services such as Netflix; and as a result, this makes it all the more riskier for networks to try and deviate from what works. 

### The Need

With the changing dynamics of media consumption by audiences, it is imperative that networks take full advantage of the historic data they have on viewership trends in order to maximize the efficacy of the shows they are renewing or newly syndicating. By evaluating the possible effects (or lack thereof) of certain features of TV shows such as the main billing actors, the genres, writers, airing time/date/season, Hollywood can make strategic decisions on what shows to proceed with and which shows to forfeit in order to min/max their control of the market. I will explore this question of whether a TV show's success can be predicted based on it's traits by using publically available metadata and evaluating those against IMDB ratings. This is a regression problem, so I intend to utilize multiple regression models (linear regression, random forest regressor, gradient boost regressor) and compare the R2 and Mean Absolute Error scores to determine the effectiveness of the model. 

### Outline
1. [Data Gathering/APIs](./Capstone/01a_Data_Gathering.ipynb)
I scraped Wikipedia for a list of TV shows from 10 different networks, which ended up being approximately 13,000 shows. These shows were then queried through 3 different APIs in order to collect as much information as possible. These files were saved as pickles to transfer between notebooks, then cleaned and categorized during the preprocessing step. There is a Data Dictionary markdown file that documents what information was found in which API, though there were a lot of overlapping and/or null fields from the three sources. 
2. [Preprocessing/EDA](./Capstone/03a_Data_Preprocessing_Cleanup.ipynb)
The data I collected ended up shrinking to between 2000 to 3000 results, dependent on the API. I sorted through the features to remove any duplicates or any fields that were not relevant to TV shows. From there, I then sorted through for missing values in the remaining features order to determine whether it could be imputed or if the observations or features would have to be further dropped. I ended up categorizing a lot of the features, both strings and numeric, as I did not want them improperly represented in the model. 
3. [Modeling/Analysis](./Capstone/04_Modeling_Interpretation_&_Conclusion.ipynb)
I trained and tested three models as my primary models to try and predict IMDB ratings: linear regression (also included Lasso and Ridge), Random Forest, and Gradient Boost. I input these models into three gridsearches in order to be able to see the effects of the hyperparameter tuning, as well as to be able to utilize two different scoring metrics; the default scorer was R2, or variance explained by the prediction. The other scoring metric was Mean Absolute Error. Although no model performed particularly extraordinarily, I the Mean Absolute Error ended up being well within one standard deviation; that being said, all of my models tended to overfit (some dramatically so), which can be attributed to the small dataset, among other factors.


### Results

| Model                   | R2         | Mean Absolute Error |
|-------------------------|------------|---------- |
| Linear Regression       | 0.233      | 0.697     |
| Random Forest           | 0.322      | 0.584     |
| Gradient Boost          | 0.411      | 0.513     |  
   

4. Summary and Conclusions
My best model ended up being the Gradient Boost Regressor, though it does have the downside of being a black-box model with less interpretability than Random Forest. However, the massive overfitting of the Random Forest model makes it essentially all but useless. 

Although a model with approximately 40% of the variance explained is not terrible using the limited features and observations that I had access to, I beleive that a better target to predict on would be viewership numbers per episode. This would allow for a significantly larger dataset size and would introduce a temporal element to the data, as well (as shows would be received differently as a season opener vs middle arc vs series final). In addition, the IMDB ratings turned out to be skewed to the left and with a relatively sharp incline/decline from the peak, indicating that there is not significant spread within the ratings themselves. Similarly, the IMDB votes gravitate heavily skewed right. This furthers the idea that IMBD ratings are not the most ideal target values, as they are entirely subjective in scale, and each individual will have their own internal rubric for what requirements merit what scores. Therefore, I would not recommend my model for production in its current state, and instead would want to optimize it towards a more consistent, measureable target value. In that scenario, I believe the model would be able to perform better.
  
    
Sources: https://cseweb.ucsd.edu/classes/wi17/cse258-a/reports/a095.pdf
         https://pdfs.semanticscholar.org/e7ae/2379489570302b28f396084b368be64db4ca.pdf
    