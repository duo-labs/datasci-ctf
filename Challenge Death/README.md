# Challenge Death
The `inquest_data.csv` dataset describes the results of coroner's inquests in Westminster from 1760 to 1799. The data source is available on [github](https://github.com/sharonhoward/londonlives/tree/master/coroners_inquests) if you want to learn more. The dataset we provide is simply a subset of the columns from the original source. We haven't otherwise cleaned or altered the data. Be warned that this challenge is about various kinds of unexpected death, and is a bit gruesome. After exploring the data, you may be grateful not to live in London in the 1700s.

A good first step with any dataset is to get an understanding of what information is in each column. In this dataset, most columns are free text fields. This means that you might not be able to rely on as much structure or consistency in the data as you might like.

Brief column descriptions

* `doc_date` - dates (which should normally be the inquest dates) in most cases have been extracted from the London Lives XML, with any missing dates filled in manually
* `parish` - The Parish where the death was recorded. These are Parishes in [Westminster] (https://en.wikipedia.org/wiki/City_and_Liberty_of_Westminster#Constituent_parishes_and_other_areas).
* `the_deceased` - the name(s) or other identifying information given for the deceased (eg "an unnamed woman")
* `given` - first name
* `surname` - last name
* `gender` - recorded gender
* `verdict` - a summary of the jury's verdict: accidental, natural causes, homicide, suicide, undetermined
* `cause_of_death` - a summary of the cause or circumstances of death
deceased_additional_info - some notes on particular characteristics of the death or event


Note: the dataset is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).