[![wercker status](https://app.wercker.com/status/5c865c33255e4e83684ac1321a73d6f0/s/master "wercker status")](https://app.wercker.com/project/byKey/5c865c33255e4e83684ac1321a73d6f0)

[![wercker status](https://app.wercker.com/status/5c865c33255e4e83684ac1321a73d6f0/s/master "wercker status")](https://app.wercker.com/project/byKey/5c865c33255e4e83684ac1321a73d6f0)

## Homework 3 - Formula 1

Due on Tuesday, February 20th by 11:59 pm.

<br/>

### Data

For this assignment you will be working with a data from the 2015 Formula 1 season. The data was downloaded from ergast.com in the form of a single large JSON file which contains information on the results of all 19 races from the 2015 season. Your repo should contain both a prettified version of the original json file (`f1.json`) as well as an RDS binary file (`f1.rds`) which can be read in using

```r
f1 = readRDS(file="f1.rds")
```

The data is structured as a list of lists of lists of lists and so on, it is up to you to look at the data and figure out how it is structured and how best to get at the information you want. There is no need to create a tidy data frame of the entire data set, you are free to manipulate and encode the data in anyway you see fit.

<br/>


### Task 1 - Describe the data

Briefly describe the structure of the `f1` object, in particular you should address what information is contained in each level of the list of lists as well as comment on any interesting or unusual features of these data.

### Task 2 - Driver standing

Using these data construct a table showing the World Drivers' Championship standings for this F1 season. This table should resemble the results available on [Wikipedia](https://en.wikipedia.org/wiki/2015_Formula_One_season#World_Drivers.27_Championship_standings). Your data frame should also have the same 21 columns: Driver name, finishing position for all 19 races, and their overall points total for the season. Failure to finish for any reason (did not start, did not finish, disqualified, etc.) should be coded as an `NA`. Race finishes and points total should all have an integer type. Your data frame should be sorted by points total, but you do not need to include any additional logic to handle ties.

### Task 3 - Constructor points

Using these data construct a table showing the World Constructors' Championship standings for this F1 season. Your data frame should have 10 rows, one for each team/constructor, and 21 columns: team name, 19 columns that contain the points earned for each race, and team overall points total. Note that a team can have multiple drivers, so the reported points should be to total of all points scored for that race. It would be a good idea to compare your computed points total to those given in the table [here](https://en.wikipedia.org/wiki/2015_Formula_One_season#World_Constructors.27_Championship_standings). Note that your table should *not* match this table as we want a single row per constructor.

### Task 4 - Visualize the season (driver)

Construct a data frame similar to the one used in task 2, but instead containing driver points for each race. Using this data frame build a visualization comparing the 21 drivers that shows their *cumulative* points earned throughout the 2015 season. This plot should have cumulative points on the y-axis and race on the x-axis with driver identified by color and/or some other aesthetic. 

### Task 5 - Visualize the season (constructor)

Using the data frame created in task 3, construct a visualization comparing the 10 teams that shows their *cumulative* points earned throughout the 2015 season. This plot should have cumulative points on the y-axis and race on the x-axis with team/constructor identified by color and/or some other aesthetic. 

