## The verdict is in
The coroner's verdict categorizes the deaths into several categories. Order the following causes from most to least numerous in a comma separated list: suicide, homicide, accidental, natural causes.

_points_: 30

**Flag**

_flag_: `\s*accidental\s*,\s*suicide\s*,\s*natural causes\s*,\s*homicide\s*`

_flag type_: regex


## Accident prone
What percent of people marked as female died from accidental causes? Round to the nearest percent (answer with a number from 0-100).

_points_: 20

**Flag**

_flag_: `31`

_flag type_: static


## Accident prone II
What percent of people marked as male died from accidental causes? Round to the nearest percent (answer with a number from 0-100).

_points_: 15

_requirement_: Accident prone

**Flag**

_flag_: `45`

_flag type_: static


## It’s complicated
The "cause\_of\_death" column has a free text description of the cause of death. Take a few minutes to explore this column. Find the longest cause of death description (by character count). What is the name of the person who died in that way?


_points_: 25

**Flag**

_flag_: `Rose Davis`

_flag type_: static


## Parish count
How many different parishes are represented in this dataset? Remember that this dataset is about Westminster, and you can look up what parishes exist.


_points_: 30

**Flag**

_flag_: `11`

_flag type_: static

**Note**

This question is about finding the number of parishes. It’s a little tricky because there is an empty string parish that shouldn’t count, and 2 parishes that are duplicated. Parish St Ann is the same as St Anne. The participant can go to [wikipedia](https://en.wikipedia.org/wiki/City_and_Liberty_of_Westminster#Constituent_parishes_and_other_areas) to verify there is only one St Anne


## Mass casualties
Most days there are at most a couple inquests recorded. However, there are three events in this dataset where 6 people died at once. What are the dates and indicated causes of death for these three events? 

Give the answer in the following format, with the events in chronological order: 17XX-XX-XX, cause\_of\_death; 17XX-XX-XX, cause\_of\_death; 17XX-XX-XX, cause\_of\_death


_points_: 70

**Flag**

_flag_: `\s*1764-04-16\s*,\s*burnt\s*;\s*1794-02-04\s*,\s*crushed in a crowd at Haymarket theatre\s*;\s*1796-06-07\s*,\s*crushed by a falling house\s*`

_flag type_: regex

**Hint**

_hint_: There are two ways to find groups of deaths. One is to look for multiple inquests that have the same date and cause of death. The other is to use the deceased_addition_info column, which has a value that indicates multiple people died.

_cost_: 5.0

**Note**

This question is about finding the 3 events where 6 people died. It’s probably the hardest question in this category. You need to find the 3 events in 2 ways. The first is to group by columns `doc_date`, `cause_of_death` and count to find the events with multiple deaths. This’ll give the events on 1764-04-16 and 1796-06-07. Note there are a total of 7 deaths on 1796-06-07 because 1 person, Thomas Coombes, died in an event different from the 6 death event.

To find the 3rd event you can filter to events with value `multiple deceased` in column `deceased_additional_info`. Then you’ll see there are multiple names in column `the_deceased` and one of the rows has 6 names.

In Google Sheets: 

1. Create a pivot table. Group by `doc_date`, `cause_of_death`, and count. Sort the rows by `COUNTA of doc_date`. Note down the two `doc_date` and `cause_of_death`s with count of 6.
2. In a column, create `FILTER` on `the_deceased` where `deceased_additional_info` = “multiple deceased”. There should be 6 rows. Find the event where there are 6 names in `the_deceased`



## Dangerous entertainment
We recently learned that Haymarket Theatre may not have been the safest place to find entertainment. How many people died at Haymarket?

_points_: 30

_requirement_: Mass casualties

**Flag**

_flag_: `11`

_flag type_: static

**Note**

This question is about ordering the causes of death from most to least frequent. It’s slightly tricky because you can’t simply search for the verb since the dataset uses different tenses. For example instead of “drowning” the cause is “drowned”. Most of the deaths by “falling” has cause “fell off <something>”, “fell down <something>” etc.

In Google Sheets:
* Create a filter view on `cause_of_death` and filter based on condition: “text contains”. Filter for the past tenses of the verb and write down the counts for each



## Common causes
The cause of death column is free text, but there are some common themes. Consider the following higher level causes of death: falling, drowning, burning, crushing, hanging. Order these causes from most to least frequent by using string matching on the cause of death column. Give the answer as a comma separated list (example: a, b, c).

_points_: 50

**Flag**

_flag_: `\s*drowning\s*,\s*falling\s*,\s*hanging\s*,\s*burning\s*,\s*crushing\s*`

_flag type_: regex


