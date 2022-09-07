# Analysis of Go Fordbike sharing system
## by Adebakin Ayub T.



## Dataset
> This analysis tends to analyze the GO Fordbike sharing system. The dataset consist of one hundred and eighty three thousnad four hundred and twelce(183412) rows(samples) measured over sixteen(16) features/variables/ columns. The Go Ford bike is a bike hiring services that matches a member with an electronic assisted bicycle to navigate the busy, in most cases heavy traffic roads so that commuting time can be reduced and efficiency can be increased as the case may be. The bike has been noticed to climb hilly roads that could have been stressful on regular byclces.
* duration_sec : the diference between the time a person hires bike and returns it at the dock which is the end time.
* start_time : the start time the bicycle is hired
* end_time : the end time the byclec is returned to the dock
* start_station_id : the station id the bike is hired from
* start_station_name : the station name the bike to hired from
* start_station_latitude : the lattitude the bike is hired from
* start_station_longitude : the longitude the bike is hired from
* end_station_id : the station id the bike returned to
* end_station_name : the station name the bike to returned to
* end_station_latitude : the station latitude the bike is returned to
* end_station_longitude : the station longitude the bike is returned to
* bike_id : the bike id
* user_type : the user type (casual or member)
* member_birth_year : birth year of the user
* member_gender  : gender of the user
* bike_share_for_all_trip : if bike share was used for all trip user made within the city

> The go fordbike dataset was used for this analysis. The dataset was wrangled to make clean and tidy the dataset in a way it will suit the analysis. Of the wrangling steps that was taken was coverting user_type to categorical variable or datatypes, removing missing values in start_station_id, start_station_name, end_station_id, end_station_name, member_birth_year and member_gender, removing decimals from birth year, start station id and end station id by extrating numbers in front of the decimal and leaving out the decimal part and start_time and end time was converted to datatime pandas object from object. Couple of variable were created such as distance using longitude, latitude and haversine formular. 

> At the end of wrangling, the dataset has over eigth hundred thousand dataset or rows (183412) and sixteen features or columns (16), some of the variables are object, numeric and categorical as needed. Start and end time are categorical datatype, longitude and latitude are floats datatype from distance is claculated which is also float and station name and id are object dtypes. There are no missing values or duplicated value in the dataset. 



## Summary of Findings

> It is interesting to see that age varies with distance in a nonlinear matter, lower ages is associated with lower distances, from lower ages to median ages are associated with higher distance travelled and higher ages experinced declined distance travelled. Also, there are higher subscribers than customers which causually use bike sharing, comparing 'member_gender' with user_type, shows there are more male subscriber than male customers, more female subscribers than female customers, more 'other gender' subscriber than 'other customers' and male subscribers being the highest gender of all 'member-genders user types'.

> One might expect interaction of age and duration_sec (total number of time the bike is hired or used) to have a linear relationship however, they are related in a nonlinear manner. lower ages at left tail end or smaller ages are associated with less time duration and middle ages with higher duration time which declined at ages above the upper quartile as age continues to increase.

> 'Customer user type' tends to have higher distance travel as age increases in a nonlinear manner also. The 'user type' has high impact above subscriber user_type as most long distance traveled is observed with customer user_type. 
The interesting thing is that subcriber user_typer (the committed to the bike sharing system) are expected to have longer distance and higher time duration. However, 'customer user_type' have longer distance and higher duration time as age increases which is done in a nonlinear manner. For both distance and duraction_sec vs age by user type or member gender, lower tailed ages tends to have small distance and duration, from lower to middle ages higher distance and longer duration time and upper tail ages experienced less distance travel and duration time 

## Key Insights for Presentation

> The interesting thing is that subcriber user_typer (the committed to the bike sharing system) are expected to have longer distace and time duration. However, 'customer user_type' have higher distance and duration time as age increases which is done in a nonlinear manner
> There are more loyal customers(subscriber) than causual users (customer)