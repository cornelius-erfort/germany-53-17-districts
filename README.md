# germany-53-17-districts

This repository provides historic, comparable county-level election results for West Germany. The final dataset contains estimates for the vote share for each election since 1953 (within the boundaries of the 2017 counties). The conversion of past into current counties benefits from the way that German counties were modified: Usually two or more old counties were merged entirely into a new one.

In order to convert historic election results into the 2017 counties, I use geodata. More specifically, I calculate the share of historic counties that lie within the boundaries of 2017 counties. Subsequently, I multiply these shares with the election results of each year.

This repository also contains the conversion tables of (West) German districts (Landkreise und kreisfreie Städte) since 1953. The columns correspond to the 2017 counties, whereas the rows correspond to the counties of the specific year.

The final dataset "election-results-53-17.dta" contains the vote share for all major parties for each election since 1953. Counties are identified by an ID ("AGS"). The file "AGS-countynames-2017.dta" can be used to add the county names.


### Example: Recklinghausen

In order to demonstrate the logic behind the conversion, the following image illustrates the conversion of 1953 counties to the 2017 county "Recklinghausen" (in red). We can see that most 1953 counties were almost entirely merged into the new county. Recklinghausen (2017) is mostly made up of the counties Recklinghausen, Stadt (1953) and Recklinghausen (1953).  Only small fractions of other adjacent counties were added to the newly formed county. This is a pattern that can be observed throughout West Germany: tow or mroe smaller counties are merged into larger ones, often cities and the surrunding rural areas are combined. 

*Example of conversion of old into new counties for the county "Recklinghausen*
<img src="https://github.com/cornelius-erfort/germany-53-17-districts/raw/main/conversion_example.png" width="80%">


### Correlation of registered voters

The following graph shows the correlation of registered voters over time. There seem to be no sudden changes in the size of the electorate suggesting that the conversion works quite well.

*Correlation of the number of registered voters over time*
<img src="https://github.com/cornelius-erfort/germany-53-17-districts/raw/main/corrgram_registered_voters.png" width="80%">

### Correlation of CDU/CSU vote share

The same applies to the correlation of the CDU/CSU vote share.

*Correlation of the CDU/CSU vote share over time*
<img src="https://github.com/cornelius-erfort/germany-53-17-districts/raw/main/corrgram_CDU.png" width="80%">







## Author information

*Cornelius Erfort*

Humboldt University Berlin

Department of Social Sciences
<br>
Chair of Comparative Political Behavior

Unter den Linden 6, 10099 Berlin, Germany

Email: cornelius.erfort@hu-berlin.de
