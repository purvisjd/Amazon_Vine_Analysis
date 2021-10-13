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
![vine reviews](https://user-images.githubusercontent.com/85641017/137141949-cab5e18f-5648-4cbb-84e5-0475e563d2c3.png)
![non-vine reviews](https://user-images.githubusercontent.com/85641017/137141973-9c3e2b9a-da1e-48df-a520-46b335caf196.png)

*  The next part of the analysis was to determine how many five star reviews were represented in each subset:

   *  Vine reviews:

    ![paid five stars](https://user-images.githubusercontent.com/85641017/137143080-40f06202-7931-4d03-8c13-838915a84b3f.png)

   * Non-Vine Reviews:
 
   ![unpaid five stars](https://user-images.githubusercontent.com/85641017/137143262-31d79bfc-2bb8-43f9-bb48-e192ecb0c487.png)

*  Finally, we were able to determine the percentage of Vine reviews that were five stars as well as the percentage of non-Vine reviews that were five stars:
 
    *  Vine Reviews:
      
      ![Vine percent](https://user-images.githubusercontent.com/85641017/137148408-eec2154d-1534-48ff-8a59-a14c54cab03b.png)

   *  Non-Vine Reviews:
      ![unpaid percent](https://user-images.githubusercontent.com/85641017/137148485-e1e51bec-04b2-4397-91d8-5e563140714e.png)

* To provide further overall analysis of potential bias based on paid vs. unpaid, the total five-star votes between both sets was obtained and the the respective categories percentage of those votes was calculated as well:

   *  Total Five Star votes:
      
      ![total five star reviews](https://user-images.githubusercontent.com/85641017/137148854-1f2e53c7-88c5-43e7-959b-43d7e23992b4.png)
   
   *  Vine percent of total:
   
      ![total vine percent](https://user-images.githubusercontent.com/85641017/137148981-b6ce30e6-58a6-4b09-b796-2bda38bc1199.png)
   
   *  Non-Vine percent of total:
   
      ![total unpaid percent](https://user-images.githubusercontent.com/85641017/137149042-5fe58020-3869-4ebd-bcb8-719235c39e2e.png)
 
##  Summary of Findings:
Based on the results of this analysis, there does not appear to be any significant indication that there is a positivity bias for Vine reviews.  When looking at the Vine reviews alone, only one review out of 4 was listed as a five-star review which does not represent a significant portion of a smaller dataset.  In addition, when the single five-star Vine review is compared as a portion of all five-star reviews, it represents less than .2%.  The non-Vine reviews, at least with the selected dataset, represent a much larger collection of five-star reviews and would indicate that payment does not appear to be a significant factor in positivity bias.  Particularly when comparing the total of all five-star reviews for non-Vine reviews (94.09%) to the less than .2% for Vine reviews.  These same calculations should be run on different datasets to see if there may potentially be an increased potential for positivity bias based on product type. It would also be advisable to do an analysis of all datasets combined to get a more complete picture of positivity bias across all product types to determine if there is a correlation.  
