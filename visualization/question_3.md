# Question 3

The dataset does not define the average resolution time explicitly. Thus, we need to add a new columns to the dataset with this information. Tableau is able to compute new dimensions using the existing ones. Since we compute a difference between timestamps, we use the build-in function `datediff` to get a proper result.

## Question 3.1: average resolution time

The question refers to the average resolution time. No other dimensions are involved. We can simply take the average over all entries, after filtering out the null entries.

The visualization is just a number that represent the average resolution time of the incidents, expressed in minutes. [TODO: shall put hours here? … add unit explicitly] The visualization answers the question. The visualization is easy to read (it is just a number).

## Question 3.2: type with lower resolution speed

### Attempt 1

The first trial is `horizontal bars`. The x axis represents the average resolution time, while the y axis the type of incident. It is easy to notice that some types have a much lower or higher resolution speed than the others. However, it is difficult to understand which types have the similar resolution times. To solve this problem, we sort the types by increasing average resolution time.

The visualization answer the questions. Types `vice calls` has the fastes resolution time (about 20 minutes). `false alarms` resolution time is also low (about 50 minutes). Most types vary from 1 hour to 2 hour and 30 minutes. `public gatherings` and `homicide` take on average much longer.

Durations in minutes are difficult to read if they are greather than 1 hour. We need to format it to hours and minutes. Unfortunatelly, there is no such functionality in Tableau. There are workarounds (https://community.tableau.com/thread/154812) for computing the single value, but not for aggregations.

### Attempt 2

The `horizontal bar` of attempt 1 takes too much space on the screen (since there are a lot of types), so it is difficult to get the entire picture at the same time. We swapped the axes and got a bar chart that fits on the screen. The drawback is that the labels of the types are now vertical and more difficult to read.

### Attempt 3

Add color for types (overloading). No clear advantage… maybe only noise.

### Attempt 4

Add labels with duration to read plot better. TODO: verify if ok. (working on horizzontal version, not very well on the vertical one).

## Question 3.3: resolution speed depends of the time period

### Attempt 1

