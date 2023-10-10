# project1_group6

This is our UT Bootcamp project1. We are in group6.

Project1_Jacky.ipynb
This file anaylizes the data downloaded from espn.com regarding the attendance of different teams, games, years of NFL, NBA, MLB. and trying to find out which sport have the most attendance on average per game in United States.
  Data Sources:
	  https://www.espn.com/nfl/attendance
	  https://www.espn.com/mlb/attendance
	  https://www.espn.com/nba/attendance
  Resources files:
	  mlb_attendance_2017 - 2022.csv
	  nba_attendance_2017 - 2022.csv
	  nfl_attendance_2017 - 2022.csv
  More explanation for the csv tables generated from about url.
	  The GMS, TOTAL, AVG, PCT columes are the home data;
	  The GMS.1, AVG.1, PCT.1 columes are the road data;
	  The GMS.2, AVG.2, PCT.2 columes are the overall data.
  Data cleaning process:
	  1.Read csv files in Resources folder, and re-formating the string values to integer so that we can make some calculation after that.
	  2.Use average attendance of each home team data and get the average value of the whole set to represent the average attendance of the sport.
	  3.Merge the the average data into a new dataframe and build a plot based on it.

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


NFL, Super Bowl & Sports Betting


Question - Has sports betting impacted viewership of the Super Bowl and the sport itself?

Most of the research on paper with in-access to the underlying datasets. Reached out to a few authors on sites such as Statista and the American Gaming Association with no response. Sports Betting has developed into a huge market in North America, with state-wide legislation placed, approved, and accepted in 2017 for majority of the states in the US. In Canada, Sports Betting was legalized in 2021 so the underlying reporting data still needs a few years of maturation. Sports betting in the early 2010s was an approx. $100 million legal market and was legalized in 2017. Since the census in 2022, Sports betting within the NFL has increased participants of approx. 70 million people with a sizable increase YoY. Furthermore, the market has increased total to approx. $200 billion plus with the NFL and Super Bowl holding the largest amounts of bets, and viewership of all time. Super Bowl LVI had approx. $1.1 billion worth of bets placed in the entire 2022 season accumulating a total of $7.6 billion of bets. The 2023 season, till August, accumulated $6.2 billion of bets alone, with the next year’s playoffs occurring in that timeframe. Overall, the NFL and College football leads the entire segment with a total of 28.8% of the market share.

References
- Super bowl ratings and viewership, all-time	https://www.sportsmediawatch.com/super-bowl-ratings-historical-viewership-chart-cbs-nbc-fox-abc/
- Sports Betting Revenue Tracker: US Betting Revenue & Handle By State (legalsportsreport.com)	https://www.legalsportsreport.com/sports-betting/revenue/
- Nearly 73.5M American adults will bet on NFL this season, survey says - ESPN	https://www.espn.co.uk/chalk/story/_/id/38338437/nearly-735m-american-adults-bet-nfl-season-survey-says
- Football's Big Game: Charting Super-Sized Bets (2013-2022) (visualcapitalist.com)	https://www.visualcapitalist.com/super-sized-bets-for-footballs-big-game/
- How Sports Betting is Driving Fan Engagement and Viewership (variety.com)	https://variety.com/2022/sports/tech/how-sports-betting-is-driving-fan-engagement-viewership-1235460169/#:~:text=%25 of Sports Gamblers Who Watch,When Betting on a Game&text=CRG Global found that two,when they have a bet.
- The Explosive Growth of Sports Betting (visualcapitalist.com)	https://www.visualcapitalist.com/sp/the-explosive-growth-of-sports-betting/


Code Readme 

NFL&SportsBetting.ipynb
-	'pd.set_option..' to max out the DataFrame and read all columns and rows - pulled from stackoverflow and bingchat
-	'fig, ax1 = plt.subplots()' & '..twinx()' structure pulled from stackoverflow/chatgpt. Legend handling code 'lines, labels ....er left') pulled from BingChat/Stackoverflow in relation to subplots() function usage
-	Piechart color codes pulled from BingChat
-	Restructured the percentages "%" in the piechart due to valueerror occurrence. utilized chatgpt for '..str.rstrip('%')' to remove the trailing character on the number and reassign astype to float
-	Figsize adjustment as well as margin size adjustment from chatgpt to fig 'cropping' on saved figures - to no use, figures in presentation still cropped after multiple adjustments.
