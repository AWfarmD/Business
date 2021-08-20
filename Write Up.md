### Incentivized Reviews Radar

**Abstract**

______

The Goal of this project is to pitch Amazon a solution to their long term problem: incentivized reviews are still showing up on their product pages.  The proposed solution consists of data science and non-data science approaches: starting with a system that tags abnormal review activities, then a Natrual Language Processing model to analyze the review text, and finally to a real person for further investigation and final decision making.  The data from the website, https://nijianmo.github.io/amazon/index.html#subsets were used to perfom preliminary analysis.<sup>1</sup>  After exploring the data in Google Sheets, visualization were created with Tableau.



**Design**

____

Amazon stopped allowing incentivized reviews (The ones that clearly states they are incentivized by sellers to leave reviews) in October 2016.  After the ban, the incentivized reviews have gone underground to avoid being caught and penalized by Amazon.  There are sellers in social networks such as Facebook who are looking for reviewers for their products, and the reviewers were incentivized through PayPal.<sup>2</sup>  This practice has made it very difficult to catch incentivized reviews.  So how can we detect these incentivized reviews from a pool with millions of reviews?



**Data**

____

Data from this website, https://nijianmo.github.io/amazon/index.html#subsets were utilized for this project.  The raw data were broken down into smaller pieces with Python as the size was too big for Google Sheets to open it.  Two datasets were used: One with reviews from June 2017 to Dec 2017 with 59,003 rows (Only used half a year because the file size (17.8 MB) is close to the maximum (20 MB) for a single Google Sheet to load), the other for year 2018 with 41,807 rows.  Each row is a review.

The raw data contain 12 columns: rating, verified purchase or not, review time (yr, mo, day), reviewer id, reviewer name, product id, product style, review text, review summary, unix review time, review helpful vote, and image.  I planned to drop reviewer name and image, and kept the rest 10 columns when I dicided to use the data.  I thought unix review time will provide me the exact time for the review.  However, after converting, it is actually providing the same info as review time with only year, month, and day.  I ended up dropping it, and the cleaned datasets are both with 9 columns with 58,881 rows for 2017 and 41,783 rows for 2018.

Datasets for 2017 was only used to check if customer - A1LA4K5JF78BER had any reviews in 2017 since his/her reviews in 2018 started in January.  



**Impact Hypothesis**

____

84% of shoppers trust online reviews. <sup>3</sup>  However, incentivized reviews are biased and less likely to give products negative feedbacks. <sup>4</sup>  Customers may buy something that is not as great as they think after reading many undetected incentivized positive reviews which leads to decrease in customer satisfaction and trust, and Amazon may incur more expenses processing returned products becuase the customer do not want their purchased items anymore. The impact hypothesis is by clearly marking the reviews as 'incentivzied review,' Amazon will be able to improve its customer satisfaction and credibility, and decrease its expense regarding return processing.  



**Data Science Solution** 

____

My proposted solution is to have a system that flags abnormal review patterns, and send them to a natural language processing model that was trained/validated/tested from a database of incentivized reviews collected before the incentivized review ban in October, 2016 to analyze the tone, language, structure, and meaning of the review texts, and classify if the review is incentivized or not. 



**Other Solution**

____

* If the NLP model classifies the reviews as incentivized, then they will be directed to a real person for further investigation (to make sure if there is any activities that may affect review pattern at the time, such as a big promotion) and final decision making. 

* As more and more incentivized reviews were dealed through social networks such as Facebook, WeChat, etc, and incentivized through PayPal, Amazon can collaborate with them to identify which sellers are getting reviews through these means, and take further action.



**Measure of Success**

____

*Technical*

To validate the project, the trained NLP model will be tested with the database containing incentivized reviews discovered after the ban in October 2018.  If the model correctly identify a certain percentage of incentivized reviews (will be decided later during project roll out), and is performing better than the current model, it will be considerred successful.

*Non-technical*

The project will be considerred successful if Amazon's expenses regarding return processing decreased by a certain percentage which will be decieded later. 



**Risk and Assumption**

____

A potential risk of this project is marking genuine reviews as incentivized, and the project is based on the assumption that it is possible to decipher if a review is incentivized based on the review patterns and the structure, meaning, and tone of the review texts.  Many things can affect the review pattern of a product, such as a promotion may cause many people to purchase a product and resulting in many positive reviews.  This is why it was mentioned above after the NLP model determines certain reviews are incentivized, a real person still need to perform further investigation and then make the final decision.



**Future Steps**

____

If the project turns out to be successful, similiar model can be utilized on other websites (Yelp, Google My Business, eBay, etc) where customer reviews play a big role in the companies' services.  



**Algorithms**

____

Data cleaning and wrangling and exploratory analysis were perfromed through Google Sheets and visualization was created with Tableau.



**Tools**

____

* Google Sheets for EDA
* Tableau for visualiztion



**Communization**

____

Preliminary findings and visuals will be presented with Keynote preventation.



**Reference**

____

1. Ni, Jianmo et al., "Justifying recommendation using distantly-labeled reviews and fined-grained aspects", *Empirical Methods in Natural Language Processing (EMNLP)*, 2019., https://nijianmo.github.io/amazon/index.html#subsets,  Accessed 9 August 2021.
2. Nguyen, Nicole. "Her Amazon Purchases Are Real. The Reviews Are Fake.", *BuzzFeed News*, 20 November, 2019., https://www.buzzfeednews.com/article/nicolenguyen/her-amazon-purchases-are-real-the-reviews-are-fake, Accessed 17 August 2021.
3. Bloen, Craig, "84 Percent of People Trust Online Reviews as Much as Friends. Here's How to Manage What They See.", *Inc.*, 31 July, 2017., https://www.inc.com/craig-bloem/84-percent-of-people-trust-online-reviews-as-much-.html, Accessed 19 August 2021.
4. Statt Nick, "Amazon is cracking down on biased customer reviews", *THE VERGE*, 3 October, 2016. https://www.theverge.com/2016/10/3/13155578/amazon-incentivized-reviews-ban-vine-program-product-bias, Accessed 19 August 2021.

