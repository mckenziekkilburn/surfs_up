# Surf Shop Analysis 

#### Background

- After visiting Hawaii we wanted to see the posibility of opening a surf and ice cream shop. We need to gather information for our investor and any concerns that could help determine if the shop is a smart investment or not. One of the factors that we need to look at are the weather trends at the island, and potentially other surrounding islands, that we would like to place the shop at. Specifically precipitation is one of the weather conditions that we are focusing on. 


#### Purpose of Analysis 

- After gathering the desired data for the investor, he has asked for more information. He would like to learn more about temperature trends before opening the surf shop. Specifically, he wants temperature data for the months of June and December in Oahu, in order to determine if the surf and ice cream shop business is sustainable year-round.

### Code used for the Month of June and December
- After creating code using Python, Pandas functions and SQLAlchemy we were able to filter the date column of the Measurements table in the in the .sqlite database to retrieve all the temperatures for the month of June. 
- I was able to accomplish this code by using the following line of code: 


                                         ``` results = session.query(Measurement.date, Measurement.tobs).filter(extract('month', Measurement.date) == 6).all() ```
                                         
                                      
- I used this code block because I needed to be able to single out one month of each year. The == 6 and .filter helped me accomplish singleing out the month of June. 
 
- _After figuring out the code for the month of June, there were only a few changes that needed to be made for finding December. Instead of using == 6, we changed it to == 12. It was pretty much the same concept just some values needed to be changed to filter the results to only show for the month December._

## Summary of Analysis Results

##### For the month of June, from 2010-2018,  the average temperature was 74.9, with a high of 85 and a low of 64.
##### For the month of December, the average temperature was 71, with a high of 83 and a low of 56.

>As we can see in our results, temperature for both times of the year is essentially the same. Therefore, it does not play a big role in the decision making process. 
