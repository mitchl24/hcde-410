# A1 — Working with Open Data

**Dataset:** Burke-Gilman Trail Counter North of NE 70th St
**Source:** https://data.seattle.gov/Transportation/Burke-Gilman-Trail-north-of-NE-70th-St-Bicycle-Cou/2z5v-ecg8/about_data  (pulled 2026-10-14)
**License / Terms of Use:** Public Domain

**A1 Assignment License:**
MIT License

Copyright (c) 2022 Jonathan Morgan and Brock Craft

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Questions I Asked

___

**Q1. When is the trail busiest, and when is it quietest?**
Decide what *busy* means to you first — a single hour? a stretch of the day? bikes and peds together, or separately? — and say why you chose that.

**My Response for Q1:**
A busy time of the day would represent a stretch when there is most traffic occurring, whether that's car traffic, foot traffic, bike traffic, etc. A quiet time of the day would be when there is lighter traffic and a smaller count of people.

From the graph above, the absolute maximum for pedestrian traffic is 9:00AM, but another local maximum is 4:00PM. For bikes, the absolute maximum is at 5:00PM, but another local maximum occurs at 8:00AM. Additionally, we can see the total count of people for both bikers and pedestrians begins to increase at 5:00AM, and starts to decrease for both around 4-5:00PM.

With these observations, I would conclude the trail is busiest between 8:00AM to 5:00PM, as that is where they reach their peaks. If someone was interested in exploring the trail at a time where it is quiestest, I would suggest either before 8:00AM when traffic is only starting to increase, or after 5:00PM where traffic is gradually decreasing.
___

**Q2. Do cyclists and pedestrians use the trail at different times of day?**
Compare their hourly patterns. If they differ, what might explain it?

**My Response for Q2:**
Despite sharing mostly similar data, cyclists and pedestrians do not always use the trail at the same time of day! As I was saying in Question 1, the total cyclist count reaches a maximum around 5:00PM, whereas the total pedestrian count reaches a maximum around 9:00AM. Also, the total count of pedestrians very slowly goes down between 9AM to 3PM, right before slightly increasing at 4PM, and then going doing again. For cyclists, it briefly dips around 9AM, but then only increases until 5PM, right before it sharply goes down.

Focusing on the cyclist data, cyclists use the trail the most in the afternoon and early evening. I would determine that it is increasingly popular as the day progresses, possibly due to commuting and that biking can cover farther distances. And the later it gets in the day, the more and more people get off work, and/or use the trail after work. Moreover, the sharp decline at the end of the day for cyclists is likely due to the lack of sunlight and how quick darkness overcomes the city after sunset.

Focusing on the pedestrian data, pedestrians use the trail most in the early morning and afternoon. I would determine that it's most popular then because people prefer to walk leisurely in mornings, as they are aware of warmer temperatures in the day, and greater traffic of people (and as we can see, cyclists are more active in the afternoon and evening, which is **not** when pedestrians would want to walk).

___

**Q3. Commuting or recreation?**
Is there evidence people use the Burke-Gilman to *commute*, not just for fun? Compare **weekdays vs. weekends**, and maybe morning vs. evening. Define what a "commuting pattern" would look like in the data, then say whether you see it.

**My Response for Q3:**
A "commuting pattern" in the data would mean there is a consistent total count of pedestrians and cyclists seen throughout the weekdays, and the weekends serving as a larger/smaller count of people. This is because we should expect to see the same number of commuters on Monday through Friday, and a jump or decrease in that amount for leisure on the weekend.

We can see there is a significant jump in bikers and pedestrians using the trail on Saturday and Sunday (with the peak of both being Sundays). From this data, we can assume the Burke-Gilman Trail is more likely to be used for recreation on weekends. However, there is a consistent pattern of roughly 15,000 pedestrians and 45,000 cyclists who use the trail on weekdays. This means there *is* a commuting pattern if we're finding close to the same number of people using the trail Monday through Friday.

___

**Q4. Direction and flow.**
The counter records **north vs. south** separately. Are mornings mostly one direction and evenings the other? What would that tell you about who's using the trail and where they're heading?

**My Response for Q4:**

The two graphs report how many cyclists and pedestrians are using the trail at each hour and the direction they are heading.

For the South graph, it is apparent that most cyclists use the trail to head South in the evening and early afternoon. From this, we can assume that most individuals who use the trail are commuting home to Seattle. Or, they live North, and are leisurely riding their bike after work along the rail.

For the North graph, it is a little trickier to decipher what is happening. I would say the graph is pretty similar to the total count of cyclists and pedestrians regardless of direction as they both follow an "M" shape. However, it is clear that cyclists heading North in the middle of the day are likely biking leisurely rather than commuting to work. 

Honestly, I would say from the graphs I've created that pedestrians are not really using this trail for commuting, as it is consistent amongst the data that regardless of direction, the number of people remains the same.

It's also important to note that some of the trail does not go directly North & South, it actually goes West or East, which raises questions about how the data determines what is North or South, and *where* those areas are that people are heading those directions.

___

In 3–4 sentences, name **one limitation or bias** in this dataset and how it could mislead someone who trusted it uncritically.

**My Response:**

I mentioned a few of these in my responses. One limitation in this dataset is that it does not track how many times one person might pass through a sensor. One individual could have passed a sensor five times within a few minutes, and the sensor is considering that as "five bodies", when it's really just one body, so the high number of "bodies" is deceiving. Another limitation is that as I said in the previous question, the data only collects people heading North or South, and not West or East. This is not a full or accurate representation of where people are heading using this trail if they were only heading North for a moment and then diverted East. A third limitation I could think of is that it does not track how long people are spending on this trail. 10,000 people could be spending only several minutes on the trail, but 1,000 are actively on the trail for an hour, so it's not accurately reporting what areas of the trail will garner more foot traffic.

___

## How to re-run
Open `A1.ipynb` and run all cells (needs `requests`, `pandas`, `matplotlib`).