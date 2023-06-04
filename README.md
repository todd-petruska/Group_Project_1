# Group_Project_1
## Analysis of Crime Statistics from 2018-2022 in New Orleans, Louisiana. 

For this project, we decided to look into data from police reports in New Orleans from before the Covid-19 pandemic, during Covid-19 pandemic, and after Covid-19 pandemic. The data provided from the police reports were in csv files for each year. 
 
We started by reading in the 2018 csv file into a Jupyter Notebook to experiment with our cleaning and plotting processes for one year. We ran through our data to better understand it. We looked for the data types, and the length of the dataset. There was a timestamp in the original dataset for each call received from the department. The datastamp was given as month/day/year and then hour:minutes. We cleaned the DataFrame so there was only the year, month, and day.

With a better understanding of the data, we started the deduping process. We need to see how many duplicates were in the data. We started with a count of the columns. We decided to use the Item Number column as the unique value column. We made code that would keep the first value of a row with the same Item Number and then get rid of the duplicates. We went from 122,529 rows to 72,050 rows. Under Signal Description, some of the values said "Miscellaneous Incident". We didn't know how to define that, so we removed it from the DataFrame. Finally, we only wanted to use some of the columns, so we kept Item Number, Year,	District,	Signal Type,	Signal Description,	Occurred Date Time,	Offender Gender,	and Victim Fatal Status. 

For our analysis, we wanted to focus on the types of crime, the location of the crime, and the gender of the offender. For type of crime, we counted the number for each type of crime under Signal Description, and made a DataFrame from it using the groupby function. Then we filtered to a list of the top ten crimes. We made a bar graph with the top ten crimes and then created a png file to go in another folder on a computer. 
