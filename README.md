## Introduction
FIGMA is a collaborative interface design tool used by product designers, UI/UX teams,
and developers to create digital designs (apps, websites, dashboards, etc.) in real time.
They also own FigJam (for brainstorming and whiteboarding).

Even though they are a design tool, they run as a business and like any business with a content strategy (especially on YouTube), they rely heavily on data to make decisions.

## Note: This project uses publicly accessible real-world data from the YouTube Data API — no private or confidential information was accessed.

A Youtube API allow access to the data but due so some channel and API security issue, we are about to scraped (147 by 13) real world data and a channelid was gotten from a youtube channel (FIGMA). The data contains unnecessary columns which was to cleaned using python. (FIND THE ATTACHMENT OF THE DATA ALONG THIS PROJECT). 

## Tool used (libraries)

1. PANDAS
2. NUMPY
3. MATPLOTLIB
4. SEABORN
5. PLOTLY EXPRESS
6. SCIKIT LEARN

## Analysis 

Firstly, observation were made in describing the data marking out that median are useful when filling empty space in the numerical data in order to avoid the data being sensitive to outlier. it consist of mean, variance, standard deviation and the quarters involving the min and max of the data for each numerical column. Dropping unnecesarry column inorder to center the focus of the analysis. 

secondly, different methods are used for training the data inorder to predict the views for future data. A firstly used method is the linear regression model. A linear regression model was used to train the data through the available data in order to see maybe it can be used more preferably than other model. And in the observation we made, we are able to come out that the mean square error was so large and the R-square is so much negative that we can't use it in training the model with the data inorder to avoid unprecise prediction.

For Linear regression,

        Mean square error: 7513620359.5871105
        R² Score: -3.349076579166397
        
Furthermore, some other model were considered like the RANDOM FOREST MODEL and GRADIENT BOOSTING. The model was preferable so some extent compare to linear regression model because the mean square error is smaller,Giving the root mean square as the square of the mean square error so this give the mindset of been closer to the accurate result but not accurate about the prediction. 

For Random Forest,

        MSE: 397351833.4306732
        R² Score: 0.7700025460752542 
        
For Gradient Boosting

        MSE: 616057727.3417592 Giving the root mean square to be 
        R² Score: 0.643409953501596
        
-- calculation of Root mean square is done below the analysis for confirmation

Through this testing we are able to choose the best model for training our data. I observed that Random forest will be best since it has R-square score of approx 77% compare to Gradient Boosting which has R-square of 63%. 

Random forest model is more precise with the prediction. in testing it, a given data is used, and a predicted data is used. 
on using the last value of both Likes and comments(9477, 124), we able to come up with outcome of 1455006 views so precise and actual value is 1458165 views. 

Now for Predicted value (10000,200) gives the value of 1460146 views. 

Further more, I was able to make some grouping of videos from the title and it was grouped into design and development, product update, community/fun, education and others(including news, app updates and reels e.t.c)
Thirdly, Some graphical representation of the whole analysis shows that there is a strong correlation between likes,comments and views (check the correlation matrix), Hypothesis testing proofs it right.

Correlation Coefficient: 0.5721

P-value: 3.7545e-14

Reject the null hypothesis: Significant correlation exists. 

## Recommendations:

1.  Increase the production of design and development videos to meet audience interest and drive higher engagement
2.  Leverage Best Performing Tags and Titles Reuse keywords and hashtags from videos with both high views and high engagement rates.
3.  Encourage Interaction, Add clear CTAs(call to action) in captions or videos asking viewers to comment or share, especially for videos already trending in likes.
4.  Posting More of the High-Engagement Video Types Focusing on content formats and topics that historically get the highest likes and comments.
5.  Making videos on how to integerate Automation in the design if possible this will boost the interest of people in viewing the view to increase views and likes

## In conclusion, 
The analysis confirms that the observed trends align with theoretical expectations, validating the model’s predictive accuracy and reinforcing the underlying mathematical relationships.
