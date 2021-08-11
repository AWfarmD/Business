#### Business Project Proposal ####

**Problem/Purpose**

Customers are upset when they purchase bad products due to fake reviews on Amazon, and may potentially stop using the site due to lost trust.  Amazon currently has extensive system to pin point fake reviews and prevent them from being posted on the product's page.  However, the system is not able to point out the reviews that are left by purchasers who receive incentives (Amazon gift card, seller returns a percentage of paid money back to the member, etc) from the sellers, and these reviews can be biased and potentially mislead other people to buy a product that is not as great as they think.   

This project is trying to asnwer how can these incentivized reviews be distinguished from the fake and genuine ones, and a proposed solution is having a system that is able to flag these reviews as incentivized ones.  The impact hypothesis is by clearly flagging the reviews, these reviews can provide more accurate information on products, and members can feel more confident making their purchases. One potential risk of this project is flagging genuine reviews as incentivized, and the project is based on the assumption that it is possible to distinguish the difference among the three types of reviews.   A validation process can be sending out surveys asking reviewers if they receive incentives from the sellers for leaving positive reviews, and a measure of success would be to flag 10% of the incentivized reviews. 

**Data Description**

* I plan to use the Amazon review data from this website, https://nijianmo.github.io/amazon/index.html#subsets, and columns are overall rating, verified (emailed the author to clarify if this means the reviewer made a verifed purchase if the value is True), review time, reviewer ID, Amazon standard identification number (specific number for each product), style, reviewer name, review text, summary, vote (helpful votes of the reivew).
* A sample analysis is to see whether there is a significant amount of positive reviews for a product comparing to other products. This may signal that some of the reviews are from members who received incentives from the sellers.

**Tools**

* Google Sheets for EDA
* Tableau for visualization

**MVP Goal**

A minimum viable product could have some findings and corresponding visualizations from the exploratory data analysis.



