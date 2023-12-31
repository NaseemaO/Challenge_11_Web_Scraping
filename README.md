# Challenge_11_Web_Scraping and Data Analysis. Mars.
Findings about planet Mars.
_______________
There are 12 months.  
A Martian Day is called 'Sol'.  1867 sols worth of data were looked at in this analysis. 
March is the coldest month with an average lowerst monthly temperature of -83.31. 
August is the warmest month with an average monthly temperature of -68.38.
Atmospheric pressure is the lowest in the month of June, and highest in the month of September
A year on Mars appears to be about 675 days from the 'terrestrial date vs temperature plot. Internet search confirms that a Mars year is equivalent to 687 earth (The distance from peak to peak is roughly 1425-750, or 675 days.)
Mars data from the website https://static.bc-edx.com/data/web/mars_facts/temperature.html written to a csv file. 
_______________
Part 1: Scrape Titles and Preview Text from Mars News 
•	Automated browsing (with Splinter) was used to visit the Mars news site, and the HTML code was extracted (with Beautiful Soup). 
•	The titles and preview text of the news articles were scraped and extracted. 
•	The scraped information was stored in the specified Python data structure—specifically, a list of dictionaries. 

Part 2: Scrape and Analyze Mars Weather Data 
•	The HTML table was extracted into a Pandas DataFrame. Splinter and Beautiful Soup were used to scrape the data. The columns have the correct headings and data types. 
•	The data was analyzed to answer the following questions: 
o	How many months exist on Mars? 12
o	How many Martian days' worth of data are there? 1867
•	The data was analyzed to answer the following questions, and a data visualization was created to support each answer
o	Which month, on average, has the lowest temperature? The highest? March has the lowest; August has the highest. 
o	Which month, on average, has the lowest atmospheric pressure? The highest?  June has the lowest; September the highest. 
o	How many terrestrial days exist in a Martian year? A visual estimate within 25% was made. Approximately 675 days. 
•	The DataFrame was exported into a CSV file named mars_data_csv. 
_______________

Instructions: 
Background
You’re now ready to take on a full web-scraping and data analysis project. You’ve learned to identify HTML elements on a page, identify their id and class attributes, and use this knowledge to extract information via both automated browsing with Splinter and HTML parsing with Beautiful Soup. You’ve also learned to scrape various types of information. These include HTML tables and recurring elements, like multiple news articles on a webpage.
As you work on this Challenge, remember that you’re strengthening the same core skills that you’ve been developing until now: collecting data, organizing and storing data, analyzing data, and then visually communicating your insights.
What You're Creating
This new assignment consists of two technical products. You will submit the following deliverables:
•	Deliverable 1: Scrape titles and preview text from Mars news articles.
•	Deliverable 2: Scrape and analyze Mars weather data, which exists in a table.
Files
Download the following files to help you get started:
Module 11 Challenge filesLinks to an external site.
Instructions
Part 1: Scrape Titles and Preview Text from Mars News
Open the Jupyter Notebook in the starter code folder named part_1_mars_news.ipynb. You will work in this code as you follow the steps below to scrape the Mars News website.
1.	Use automated browsing to visit the Mars news siteLinks to an external site.. Inspect the page to identify which elements to scrape.
HINT
2.	Create a Beautiful Soup object and use it to extract text elements from the website.
3.	Extract the titles and preview text of the news articles that you scraped. Store the scraping results in Python data structures as follows:
o	Store each title-and-preview pair in a Python dictionary and, give each dictionary two keys: title and preview. An example is the following:
o	{'title': "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm", 
o	 'preview': "For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27."}
o	Store all the dictionaries in a Python list.
o	Print the list in your notebook.
4.	Optionally, store the scraped data in a file (to ease sharing the data with others). To do so, export the scraped data to a JSON file. (Note: there will be no extra points for completing this.)
Part 2: Scrape and Analyze Mars Weather Data
Open the Jupyter Notebook in the starter code folder named part_2_mars_weather.ipynb. You will work in this code as you follow the steps below to scrape and analyze Mars weather data.
1.	Use automated browsing to visit the Mars Temperature Data SiteLinks to an external site.. Inspect the page to identify which elements to scrape. Note that the URL is https://static.bc-edx.com/data/web/mars_facts/temperature.html.
HINT
2.	Create a Beautiful Soup object and use it to scrape the data in the HTML table. Note that this can also be achieved by using the Pandas read_html function. However, use Beautiful Soup here to continue sharpening your web scraping skills.
3.	Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:
o	id: the identification number of a single transmission from the Curiosity rover
o	terrestrial_date: the date on Earth
o	sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
o	ls: the solar longitude
o	month: the Martian month
o	min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
o	pressure: The atmospheric pressure at Curiosity's location
4.	Examine the data types that are currently associated with each column. If necessary, cast (or convert) the data to the appropriate datetime, int, or float data types.
HINT
5.	Analyze your dataset by using Pandas functions to answer the following questions:
o	How many months exist on Mars?
o	How many Martian (and not Earth) days worth of data exist in the scraped dataset?
o	What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
	Find the average minimum daily temperature for all of the months.
	Plot the results as a bar chart.
o	Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
	Find the average daily atmospheric pressure of all the months.
	Plot the results as a bar chart.
o	About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
	Consider how many days elapse on Earth in the time that Mars circles the Sun once.
	Visually estimate the result by plotting the daily minimum temperature.
6.	Export the DataFrame to a CSV file.


