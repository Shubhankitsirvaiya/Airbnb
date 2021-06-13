# Airbnb Data Analysis-

Since 2008, guests and hosts have used Airbnb to expand on traveling possibilities and present a more unique, personalized way of experiencing the world. Today, Airbnb became one of a kind service that is used and recognized by the whole world. Data analysis on millions of listings provided through Airbnb is a crucial factor for the company. These millions of listings generate a lot of data - data that can be analyzed and used for security, business decisions, understanding of customers' and providers' (hosts) behavior and performance on the platform, guiding marketing initiatives, implementation of innovative additional services and much more.

Coding Language used-- Pyhton version 3.0
Platform used - Google collab notebooks

## Data provided-

Id-  Unique Id of each property

name- Name of properties, which also describes the property 

host_id- ID of the host, this is unique for all the hosts.

host_name- Name of the host , Names may be similar for two hosts.

neighbourhood_group-  have 5 different regions of New York

neighbourhood-   these are the sub-regions of neighbourhood_group , where one neighbourhood belongs to only one neighbourhood group.

Latitude-  contains the coordinates of Latitude for that location.

Longitude-  contains the coordinates of longitude for that location

room_type– there are three types of property available.

price-   price of stay (we have taken it for one night basis).
minimum_nights-   this is the minimum number of nights for which you have to book a host’s place.

number_of_reviews-  This will be the number of reviews each property has got,we can also use this to infer about the number of customers considering the same customer behaviour across regions.

last_review-  Date of last review that is posted for the property.

reviews_per_month-   Number of reviews for each property per month.

calculated_host_listings_count-  Number of listing for each property.

availability_365-  Number of days each property is available out of 365 days of the year.



### Assumptions-
We have ignored the null values and kept them as it is as for last_review column,and for number of reviews we have taken it as 0
-null values are present in only two columns, number of review columns and last_review
-null values does not affect our code here much.
We have taken the customer_review columns to gain the idea about number of customers ,considering similar customer behavior for reviews accross all region.


###Pyhton libraries used- Numpy ,Pandas ,Matplotlib,Seaborn

# Hidden trends and pattern Found



--Comparasion of number of property in each neighbourhood group


property_count=df['neighbourhood_group'].value_counts().reset_index().

--Comparasion of number of reviews in each neighbourhood group.

review=df.groupby('neighbourhood_group')['number_of_reviews'].sum().reset_index().

--Making minimum night category.

--Converting last review to datetime and taking month from it.

--Count of number of Properties in each type of room across different groups.

--comparing mean price for manhatten and Brooklyn ,and why price is high in manhatten despite similar demand and suppply.

--Mean price for each type of room across different neighbourhood groups.

--We can Look into each Nieghbourhood Groups seperately to look deeper into subset Neighbours(top 5 on the basis of most number of host present),
here for plotting and slicing we have made a function so as to not repeat the process 5 times.


--Count of properties availabel in different price range in each neighboorhood.

#### future suggestion and ideas

--Identify High Demand areas where AIRBNB should increase supply.

--Marketing + Discounts (People can travel extra to stay here).


For more details, please see comments in code and refer the colab notebook 'Complete Colab notebook'. If you want to use this code in your lab but need help ,please feel free to comment on this file and on colab notebook.

Thanks for Reading me!!!
