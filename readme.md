For this project, I used a videogame sales dataset found in Kaggle. 

I wanted to see which factors affected the global sales of a game, and I chose genre, platform, publisher and year as my independent
variables.

I would later decide to test the data using four models, Logistic Regression, Decision Tree, Random Forest, XGBoosting and SVMs. With the purpose of testing which model yielded the best accuracy scores and could help me determine my hypothesis.

The first thing I did was turn the dependant variable into a categorical column, which had to contain True/False values.
In this case, it was whether a game got high global sales or not. The method I use to determine this was by getting the median of all global sales, but I ran into an issue, as the median of my default global sales was giving me a value of 0.17, when my highest number was 87.2; that's when I decided to do a histogram to see if the default dataset was skewed in a way.

After looking at the histogram, I understood that I had more data in the "less than 1 million" area of sales, and that my models would be likely overfitted if I didn't get rid of the highest vales, after all, I was just determining which were the factors that affected video games sales, not which game had the highest sales.

I then got the upper and lower bounds of the data and used them as my new dataset for my models, and I did a histogram with my filtered data, which was way better than what I had before.

I did some more cleaning before actually running the models, like getting rid of unnecessary columns, changing categorical sales to 1 and 0 instead of true and false, one-hot encoding and other methods.

My first model was Logistic Regression, which after training my data, I printed the accuracy score, as well as the classification report, which was repeated in each model I did afterwards. I also decided to show a heatmap to compare the TP and TN of all the models in a visual way. For later models, such as Decision Tree I decided to test if there was still overfitting by doing cross-validation with 5 repetitions, which yielded similar results as the classification results and accuracy scores. I used this same method for the remaining three models.

The best model overall was XGBoosting, and after determining this, I decided to do some cross tables to confirm the ideas of my hypothesis.
After analyzing the cross-tables, I could see that not all factors actually influenced on whether or not a game had high sales, but the ones that did were genre and platform.