library(dplyr)

library(nycflights13)
dim(flights)

filter(flights, month == 1, day == 1)
flights[flights$month == 1 & flights$day == 1, ]

arrange(flights, year, month, day)
arrange(flights, desc(arr_delay))

# Select columns by name
select(flights, year, month, day)

# Select all columns between year and day (inclusive)
select(flights, year:day)

# Select all columns except those from year to day (inclusive)
select(flights, -(year:day))

#renaming coloumns
select(flights, tail_num = tailnum)
rename(flights, tail_num = tailnum)

mutate(flights,
       gain = arr_delay - dep_delay,
       speed = distance / air_time * 60
)

transmute(flights,
          gain = arr_delay - dep_delay,
          gain_per_hour = gain / (air_time / 60)
)

summarise(flights,
          delay = mean(dep_delay, na.rm = TRUE))