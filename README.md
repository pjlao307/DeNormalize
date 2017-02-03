# DeNormalize
This is a python script to pivot survey data from multiple surveys into 1 row per user survey instance, 1 column per question and one survey per tab. All excel based.

For PEER exports (Jan 2017 Update)
Data preparation steps:
1. remove junk rows at top of survey answers table between header and data
2. replace survey id for all ** for askme users with "X"
3. replace all blank survey ids for birthdays with "0" (created survey id 0 for Birthday)
add columns S and T in Survey Responses with short survey name and survey sort code (using vlookup on survey id and look-up table you maintain)
4. Sort Survey Responses by order desired
   a. survey sort code
   b. survey name (to sort alpha when survey code is same)
   c. foreign key (to group surveys and instances together)
   d. instance
   e. date answered (to approximate question order so question columns are same)
