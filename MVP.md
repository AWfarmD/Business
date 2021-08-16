### Business Project MVP

**Problem/Impact**

This project is trying to answer how can incentivized reviews be distingueshed from genuine ones on Amazon.  The impact hypothesis is by clearly marking the review as "incentivized review," Amazon will be able to provide their customers more accurate product review ratings.

**Solutions**

* Amazon allowed incentivized reviews as long as the reviewers clearly mentioned their affiliation with the sellers in the text of the reviews in the past, and this practice was stopped by Amazon starting October 2016.  Amazon can create a database with these self marked incentivized reviews, and use it to train/validate/test an NLP model that can classify reviews with similiar tone, language, and meaning as incentivized reviews. 
  * Amazon can have a system to detect unusual increase in 5 star reviews or increase in multiple reviews from the same customer within a short period of time, and then use the above model to make the classification.
* As more and more purchased reviews were dealed on social networks such as Facebook, WeChat, etc, and incentivized through PayPal, Amazon can collaborate with them to identify which sellers are buying reiewers, and then build a database to mark them with "Incentivized review" on the page.

* Amazon can provide incentives to customers who report sellers that provide incentives to get more reviews. 

**Visual**

The visuals below present a product started to rapidly receive 5 star reviews once there was a 1 star review been left at the product page.  There were eight 5 star reviews from the same reviewer on August 8, 2018, and twenty 5 star reviews from the same reviewer on August 18, 2018.