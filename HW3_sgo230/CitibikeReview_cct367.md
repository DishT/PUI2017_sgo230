# Citi Bike Review
by ChunChieh Tsai

###a. verify that their Null and alternative hypotheses are formulated correctly
The general notion is ***"Younger people are more likely to ride Citi Bikes late at night".***

And ***Null hypothesis*** is *"The proportion of riders 35+ to total riders for trips starting at midnight-5 am is higher or equal to the proportion of riders 35+ to total riders for trips starting at 5 am - midnight."*

I agree with the null hypothesis, and it fit the the notion, however, I would change the notion to **"Age below 35+ people are more likely to ride Citi Bikes late at night"**


###b. verify that the data supports the project

The repo chose "hour" and "age" as analysis target,  seperate age to 2 groups by above 35 and uuder 35, and also seperate time to 2 groups.

```
df2 = df[df['age_group'] == "35+"]
#df2.groupby('hour').size().plot(kind='bar', color='blue', alpha=0.5)

df1 = df[df['age_group'] == "<35"]
#df1.groupby('hour').size().plot(kind='bar', color='red', alpha=0.5, label='nine')
```




I would suggest not to add 2 new "string" columns,(ex: "<35" ,"35+","Day time" and "Late Night"), and use the original column.

```
df2 = df[df['age'] >= 35]
df1 = df[df['age'] <  35]

```

###c. chose an appropriate test to test H0 given the type of data, and the question asked

I would choose Chi-Square, because it is a cotogorized data and seperate to two groups.
