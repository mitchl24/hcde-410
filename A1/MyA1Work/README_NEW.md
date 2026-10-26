# A1: Working with Open Data

**Dataset:** Burke-Gilman Trail Counter North of NE 70th St
**Source:** https://data.seattle.gov/Transportation/Burke-Gilman-Trail-north-of-NE-70th-St-Bicycle-Cou/2z5v-ecg8/about_data  (pulled 2026-10-14)
**License / Terms of Use:** Public Domain

## AI Usage

I did not use AI for my work.

## How To Re-run
Open `A1.ipynb` and run all cells (needs `requests`, `pandas`, `matplotlib`).

## Limitation I Addressed

In 3–4 sentences, name **one limitation or bias** in this dataset and how it could mislead someone who trusted it uncritically.

**My Response:**

One limitation in this dataset is that the data only records the direction of travel at a single point in time, and only focuses on people heading North and South, not West or East. This is not a full or accurate representation of where people are heading using the Burke-Gilman trail if they are only tracking two out of four directions, especially since the trail bends throughout. If someone were only heading North for a moment, and then diverted East, the counter is accurately considering that as "North", but does not tell us their whereabouts or direction outside of that point. This can be misrepresentative for someone who is trusting the data uncritically as they immediately assume a direction of the trail to be busier than it actually is. For example, if someone was reviewing this data and saw Southbound traffic to be busier in the evening, they would conclude the entire trail to be busy when the data only verifies a specific point on the trail and the direction at that specific point.

## Questions I Asked


**Q1. When is the trail busiest, and when is it quietest?**
Decide what *busy* means to you first — a single hour? a stretch of the day? bikes and peds together, or separately? — and say why you chose that.

**My Response for Q1:**

I would say a busy time of the day is a long stretch where the total count of pedestrians and cyclists is above a certain threshold of people. I define it this way because each cyclist and pedestrian is counted as a "body", so it would make the most sense to assume the busiest time is when the most "bodies" are on the trail, not separating them. Moreover, choosing a long stretch of the day is better representative of how consistently trafficked the trail is rather than a single hour where it only considers the absolute peak of traffic.

From the graph above, the absolute maximum for pedestrian and cyclists combined is 5:00PM. Referring to the y-axis, a good measurement for a threshold of people on the trail is when the total count is above 10,000. We can see the total count begins to jump in the morning at 5:30AM, and is slowly reaching a minimum around 8:00PM. In between those times (5:30AM to 8:00PM) the total count/traffic is actively increasing/decreasing or consistent at a maximum of people. That being said, we can move further with another threshold and consider that the total count of people remains close to or above 40,000 between 8:00AM and 5:00PM.

With these observations, I would conclude the trail is busiest between 8:00AM to 5:00PM, as that is where the threshold of people is close to or above 40,000. I would conclude the trail is quietest between 8:00PM to 5:30AM (the next day), as that is when the threshold of people is below 10,000.



**Q2. Do cyclists and pedestrians use the trail at different times of day?**
Compare their hourly patterns. If they differ, what might explain it?

**My Q2 answer:**

Despite sharing similar data, cyclists and pedestrians do not always use the trail at the same time of day! 

Looking at the graph, the percentage of total pedestrians and cyclists in 2019 is displayed for each hour of the day. The peak time that the most percentage of pedestrians are using the trail is at 9:00AM, where 10% of total pedestrians were counted for at that time. The peak time that the most percentage of cyclists are using the trail is at 5:00PM, where 10% of total cyclists were counted for at that time. We can conclude that although pedestrians and cyclists use the trail similarly by being active during the day time, they are less likely to encounter each other in the morning (when pedestrian counts are at a peak) and evening (when cyclist counts are at a peak).

For cyclists, they use the trail the most in the afternoon and early evening. I would determine that it is increasingly popular as the day progresses, possibly due to commuting and that biking can cover farther distances. And the later it gets in the day, the more and more people get off work, and/or use the trail after work. Moreover, the sharp decline at the end of the day for cyclists is likely due to the lack of sunlight and how quick darkness overcomes the city after sunset.

For pedestrians, they use the trail most in the early morning and afternoon. I would determine that it's most popular then because people prefer to walk leisurely in mornings, as they are aware of warmer temperatures in the day, and greater traffic of people (and as we can see, cyclists are more active in the afternoon and evening, which is **not** when pedestrians would want to walk).



**Q3. Commuting or recreation?**
Is there evidence people use the Burke-Gilman to *commute*, not just for fun? Compare **weekdays vs. weekends**, and maybe morning vs. evening. Define what a "commuting pattern" would look like in the data, then say whether you see it.

**My Response for Q3:**
A "commuting pattern" in the data would mean the peak counts across the weekdays and weekends differs. This would make sense because commuting on a weekday falls under the morning and evening times where the peaks are, whereas recreation would mean people use the trail leisurely at a time where they are not commuting, on a weekend. 

As we can see from the graph, there is a significant jump in cyclists using the trail on the weekend in general. Furthermore, the peak count of cyclists is at 8:00AM and 5:00PM on weekdays, but for Saturday and Sunday that peak is found at 12:00PM-1:00PM. 

We can conclude from this data that the trail is definitely used for recreation on weekends where people have more availability (hence the high average count of cyclists), but also more freedom to choose when they want to use the trail, which is clearly in the afternoon rather than the morning or evening.



**Q4. Direction and flow.**
The counter records **north vs. south** separately. Are mornings mostly one direction and evenings the other? What would that tell you about who's using the trail and where they're heading?

**My Response for Q4:**

The two graphs report how many cyclists and pedestrians are using the trail at each hour and the direction they are heading.

For the South graph, it is apparent that most cyclists use the trail to head South in the evening and early afternoon. From this, we can assume that most individuals who use the trail are commuting home to Seattle. Or, they live North, and are leisurely riding their bike after work along the rail.

For the North graph, it is a little trickier to decipher what is happening. I would say the graph is pretty similar to the total count of cyclists and pedestrians regardless of direction as they both follow an "M" shape. However, it is clear that cyclists heading North in the middle of the day are likely biking leisurely rather than commuting to work. 

Honestly, I would say from the graphs I've created that pedestrians are not really using this trail for commuting, as it is consistent amongst the data that regardless of direction, the number of people remains the same.

It's also important to note that some of the trail does not go directly North & South, it actually goes West or East, which raises questions about how the data determines what is North or South, and *where* those areas are that people are heading those directions.
