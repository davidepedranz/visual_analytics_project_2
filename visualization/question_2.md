# Question 2



## Question 2.1: spatial distribution over years

Since we want to visualize a spatial distribution, we use a map. We filter out values without a time, since we are interested in the differences among years.

### Attempt 0

Before answering the question, let's take a look at the data. We plot the number of indicents per year. **Around 2/3 of the data have no information about the year!**

### Attempt 1 (best)

Visualize the time (years) on different maps. We have only 9 years of data, so the visualization fits on the screen. The visualization allows to easily compare different years.

#### Parameter settings

Reduce the size of the points to the minimum allowed and decrease the opacity. The zoom level is low. The combination of this factors allows to visualize the distribution of the incidents in the entire city. The low opacity level underlines zones with a higher concentration of incicents.

#### Results

In years 2009, 2010 there are almost no points. Year 2013 have much less points than the others, but seems to have a similar distribution to the other years. There is no clear difference in the spatial distribution of incidents over years.

#### Strong points

* The entire visualization fits on a single screen, so it is easy to spot similaritie, differences and trends among the different years.
* It is possible to change the order of the years to make better comparisons.

#### Weak points

* It is difficult to compare single zones of the city: changing the zoom makes the visualization confusing (there is no clear visual separation of different years). 

### Attempt 2

We try to fit the visualization on a single map to overcome the limitations of the previous attempt. We need to find a visual attribute to encode the type.

* `Size` is not the best, since we are treating the year as a categorical value.
* `Shape` is not a good choice: there are about 500.000 points on the map.
* `Color` is the choice for this attempt.

#### Parameter settings

In order to see the different colors we need to use a high opacity, otherwise they tend to mix with each other. For the same reason, we use a small size for the points.

#### Weak points

Colors tend to overlap and mix with each other, due to the high number of visualized points.

### Attempt 3

Encode each type on a different page of the visualization.

#### Good points

It is possible to visualize zoom to a specific zone.

It is possible to see the trends (changes in the distribution) as a kind of "animation".

#### Weak points

It is not possible to compare 2 years side by side.



## Question 2.2: zone with consistent low/high level density over all years?

We can use the same visualizations made to answer the previous question.

#### Results

Same distribution over years. The same answers to question 1.1 apply here.