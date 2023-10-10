# project1_group6
This is our UT Bootcamp project1. We are in group6.

super_bowl_history.ipynb
This file anaylizes the data retrieved on Super Bowl game history. So that we could compare data treands between viewership, attendance, locations and teams.
Data Sources:
-   super bowl history api pull = "https://data.opendatasoft.com/api/explore/v2.1/catalog/datasets/super-bowl@public/records?limit=54"
-   geo locations of super bowl pull = "https://api.geoapify.com/v1/geocode/search"
-   super bowl viewership = "Resources/Super Bowl Ratings and viewership, all-time.csv"
The file pulls both api's and creates data frames. The super bowl locations were made into a list from there city and state to be able to pull data from the geo api. This was due to the super bowl history api have a lot of duplicated "latitude" and "longitude" data. 
The data frames were merged together on "city" and "state".
The merge data frame "super_bowl_history_df" was cleaned by dropping many columns that were not needed. 
The super bowl viewer ship was read in from a csv file and extracted just the views which were organized by date.
Now that all three data pulls have been merged we analized attendance and viewership on two scatter plots.
The calculated correlation value for the two graphs indicated that views and superbowls had a strong relation while attendance did not. 
A map was made to locate every super bowl and the attendance held at the event. 
This analysis shows that as the super bowl continues to gain popularity and viewership these increases are not affected by location or teams. Same goes for the attendance, the attendance does not share a correlation with the games them selves and is not impacted by either teams playing or location of the game. 

NFL&SportsBetting.ipynb
- 'pd.set_option..' to max out the DataFrame and read all columns and rows - pulled from stackoverflow and bingchat
- 'fig, ax1 = plt.subplots()' & '..twinx()' structure pulled from stackoverflow/chatgpt. Legend handling code 'lines, labels ..\..er left') pulled from BingChat/Stackoverflow in relation to subplots() function usage
-  Piechart color codes pulled from BingChat
-  Restructured the percentages "%" in the piechart due to valueerror occurrence. utilized chatgpt for '..str.rstrip('%')' to remove the trailing character on the number and reassign astype to float 
-  Figsize adjustment as well as margin size adjustment from chatgpt to fig 'cropping' on saved figures - to no avail.
