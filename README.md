Professional Certificate in Machine Learning and Artificial Intelligence. Practical Application Assignment 5.1: Will the Customer Accept the Coupon?
The python code and readme file can be found at https://github.com/malayghosehajra/Will-the-Customer-Accept-the-Coupon.git

**Context:**

Imagine driving through town and a coupon is delivered to your cell phone for a restaraunt near where you are driving. Would you accept that coupon and take a short detour to the restaraunt? Would you accept the coupon but use it on a sunbsequent trip? Would you ignore the coupon entirely? What if the coupon was for a bar instead of a restaraunt? What about a coffee house? Would you accept a bar coupon with a minor passenger in the car? What about if it was just you and your partner in the car? Would weather impact the rate of acceptance? What about the time of day?

Obviously, proximity to the business is a factor on whether the coupon is delivered to the driver or not, but what are the factors that determine whether a driver accepts the coupon once it is delivered to them? How would you determine whether a driver is likely to accept a coupon?

**Overview**

The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not.

**Data**

This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’. There are five different types of coupons -- less expensive restaurants (under \$20), coffee houses, carry out & take away, bar, and more expensive restaurants (\$20 - \$50).

**The Jupyter notebook coding was developed incorporating the following components:**
1. read the data file using read_csv() command
2. Evaluate the content and extent of the data set by using data.head(), data.shape, and data.info() commands
3. Any problematic and missing data was investigated using the data.isna() command. Based on this analyses, it was determined that the 'car' column can be eliminated because most of the values were null
4. Also the misspelling of 'passenger' was corrected during this stage


**What proportion of the total observations chose to accept the coupon?**
   * The proportion of observations that accepted the coupon is 56.933 %
   * The proportion of observations that rejected the coupon is  100-56.933 = 43.067 %

**Use a bar plot to visualize the coupon column**

Sanborn plotting feature was used to visualize the coupons issued versus coupon type data set.
![image](https://github.com/malayghosehajra/Will-the-Customer-Accept-the-Coupon/assets/148172622/8f0aa6d0-a2b0-4756-a00e-337a0f5cedf0)


**Use a histogram to visualize the temperature column**

The Sanborn histogram feature was utilized to develop the temperature column plot.
![image](https://github.com/malayghosehajra/Will-the-Customer-Accept-the-Coupon/assets/148172622/dbba4c97-693e-4a6a-b71e-df838afddad3)

**Investigating the Bar Coupons**

**What proportion of bar coupons were accepted?**
The porportion of bar coupons that were accepted is 41.19184526921067%

**Compare the acceptance rate between those who went to a bar 3 or fewer times a month to those who went more.**

Based on the data analysis,

a. Acceptance rate for those who went to a bar 3 or fewer times a month was 37.27%

b. Acceptance rate for those who went to a bar 3 or more times a month was 76.17%

Using plotly library a graph was created to show the histogram of bar going habits based on number of visits.

![newplot](https://github.com/malayghosehajra/Will-the-Customer-Accept-the-Coupon/assets/148172622/b2f6e416-1737-44e3-be06-bf01bd6c1834)

**Compare the acceptance rate between drivers who go to a bar more than once a month and are over the age of 25 to the all others. Is there a difference?**

a. Rate for age over 25 and more than once a month bar visit was 68.98%

b. Rate for everyone else was 33.69%


Using plotly library a separate plot was created to show the variation of bar visit in relation to the age distribution.

![newplot](https://github.com/malayghosehajra/Will-the-Customer-Accept-the-Coupon/assets/148172622/e9d7d128-f53b-47d6-b1ee-a609113d805a)


**Use the same process to compare the acceptance rate between drivers who go to bars more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry.**

a. Rate for those who go to a bar more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry was 70.94%

b. Rate for all the others were 29.66%


**Compare the acceptance rates between those drivers who: (a) go to bars more than once a month, had passengers that were not a kid, and were not widowed OR (b) go to bars more than once a month and are under the age of 30 OR (c) go to cheap restaurants more than 4 times a month and income is less than 50K.**

(a) Acceptance rate for those who go to bars more than once a month, had passengers that were not a kid and were not widowed was 70.94%

(b) Acceptance rate for those who go to bars more than once a month and are under the age of 30 was 71.95%

(c) Acceptance rate for those who go to cheap restaurants more than 4 times a month and income is less than 50K was 46.84%

**Based on these observations, what do you hypothesize about drivers who accepted the bar coupons?**


Based on the above results and graphs, I can make the hypothesis that the drivers who accepted the bar coupons were (1) younger in age, (2) no kids, (3) earned more money, and (4) visited the bars more often.

