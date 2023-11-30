## Background

Social Buzz is a fast-growing technology unicorn that need to adapt quickly to its global scale. It needs help analyzing its huge data to find the top 5 most popular categories of content. To give a background on how much data Social Buzz has been creating: - the platform receives over 100,000 posts per day which amounts to 36,500,000 posts every year of which, this is all unstructured data making it very hard to make sense of.

## Project goal

To conduct an analysis of its data to find insights regarding the top 5 most popular categories of content

## Question

Which are the top 5 content categories?

## Activities

***Understanding the datasets***

7 datasets (user, profile, location, session, reaction, content and reaction types) and a data model were provided for this project.

So, the first step was to use this data model to identify which datasets will be required to answer the business question - which is to figure out the top 5 categories with the largest popularity.

Reaction, Content, and Reaction Types were identified as our relevant data sets.

To clarify why this selection was made:

- The brief carefully states that the client wanted to see “An analysis of their content categories showing the top 5 categories with the largest popularity”.
- As explained in the data model, popularity is quantified by the “Score” given to each reaction type.
- We therefore need data showing the content ID, category, content type, reaction type, and reaction score.
- So, to figure out popularity, we’ll have to add up which content categories have the largest score.

***Cleaning the data***

Next was to Clean the data by:

- removing rows that have values which are missing,
- changing the data type of some values within a column, and
- removing columns which are not relevant to this task
  
***Data Modelling***

To complete the data modelling, a final data set was created by merging the three tables together with Reaction table as the base table, then first joining the relevant columns from the Content data set, and then the Reaction Types data set using a “VLOOKUP” formula.
 
***Data analysis & Visualization***

Using the new dataset to figure out the Top 5 performing categories, the total scores for each category were added up using the “Sum If” formula.

![Screenshot (111)](https://github.com/osby44/SocialBuzz/assets/141450625/6dd3fa8e-f126-49c2-a766-61e54c8d0f10)

***Findings/insights***

There’s a total of 16 unique categories of posts across the sample dataset, this includes Food, Science and Animals. There were 1897 reactions from just the animal category alone. Also, the most common month for users to post within was January. 

From the analysis, it is clear that the top 5 most popular categories of posts are animals, science, healthy eating, technology and food in descending order.
Animals had an aggregate popularity score of around 74965. It is very interesting to see both food and healthy eating within the top 5, it really shows that food is a highly engaging content category. Healthy eating ranks slightly higher than food, so perhaps the user base may be skewed towards healthy
eaters and health-conscious people.
Finally, its also interesting to see science and technology too. This may suggest that people enjoy consuming factual content and snippets of content that they can learn something from.

Additionally, you can see from the chart the % split of popularity between the top 5 categories. There is not much difference between the share of each category, however, the difference between the 1st most popular, animals and the 2nd most popular, science, is the largest gap equal to 1.1%.
In business terms, this could suggest that the most popular category, animals, is tailing away from the rest of the categories and may continue to get more and more popular. To avoid an issue where one content category consumes the entire platform, it will be important for you to ensure that any algorithms used to govern the content on the platform gives a fair balance to the content categories.


***Summary***

This task was tackled and the top 5 most popular categories was found as asked, but also went one step further.
- It was found that animals and science are the two most popular categories, suggesting that users like "real-life" and "factual" content
- It was also found that food was a common theme amongst popular content and the most popular food category was healthy eating. This could be a signal to show the types of people that are using the platform, and this insight could be used to boost engagement even further. For example, to run a campaign with content focused on this category or work with healthy eating brands to promote content.

Click [here](https://app.powerbi.com/links/F7P_DRYFGO?ctid=3922f60b-e8a2-4862-9142-e8910c694245&pbi_source=linkShare) to view Power BI visualization on the web.


##### Reference: Accenture Social Buzz Project
