# Amazon Prime Analysis
##  Overview of Analysis
The purpose of this analysis was to review identified datasets containing Amazon product reviews, some of which are included as part of the Vine (paid review) program.  Once a specific dataset was identified for analysis, it was then filtered to isolate those items that had greater than 20 reviews and, therefore, more likely to be helpful.  In addition, the subsequent dataset was then further filtered into those that were given the highest possible positive review (5-stars) and then divided into those that were part of the Vine program and those that were not.  Once the data was fully filtered and divided, it was then possible to run mathmatical analysis to determine the percentage of 5-star reviews that were part of the Vine program versus those that were not part of the program, thereby giving an indication as to whether paid participation in the program may have influenced positive reviews and potential bias.

##  Resources
* Data:
  * Data was obtained from Amazon AWS services.  The specific dataset used in this analysis was obtained from the following link:
  *  [Mobile Electronics Data](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Mobile_Electronics_v1_00.tsv.gz)
* Software Used:
  *  PySpark, PgAdmin, PostgreSQL

##  Results of Analysis:
*  Once the initial dataset was loaded into a dataframe and filtered, it was then further divided into two separate dataframes, one for Vine reviews and one for Non-Vine reviews:

