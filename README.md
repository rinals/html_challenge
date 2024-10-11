# html_challenge
## Source layout
* LICENSE - MIT License
* README.md
* part_1_mars_news.ipynb - News scraping Notebook
* titles_and_previews.json - Output of news scraping
* part_2_mars_weather.ipynb - Scraping weather data table for analysis
* mars_weather_data.csv - Output of weather data scraping

## Part 1 - Mars News
Packages used:
1. splinter
2. selenium web driver
3. ChromeDriverManager
4. BeautifulSoup
5. json


### Chrome Driver
Chrome browser has a Driver that can be used in python to visit web pages and explore content.
Chrome Driver version must exactly match the installed Chrome browser version. Managing this versioning can be tedious. ChromeDriverManager is used to automatically download the matching Driver version for the installed Chrome browser. It can automatically download a new Driver for any latest updates.

Once Driver path has been found, Selenium can then open browser instance to visit and explore web page content.

### Beautiful Soup
Beautiful Soup can be used to retrieve content DOM (Document object model) and identify specific sections using their 'div' tags.
Chrome Developer tab and inspect element tool can be used to identify the div tags of interest. In this case we are interested in div class "content_title" and "article_teaser_body".

### JSON result output
json package can conveniently output lists of dictionaries into json file.

## Part 2 - Mars Weather
Packages used:
1. splinter
2. selenium web driver
3. ChromeDriverManager
4. BeautifulSoup
5. matplotlib
6. pandas

### Chrome Driver
Just like in the news activity, figure out the chrome driver path to open the url.

### Beautiful Soup
Explore the webpage using Chrome developer inspect element to figure out the div tag for the mars weather table.
Find table with the class 'table'.

### Table exploration
Find the header 'th'.
Find each row 'tr'
Within each row 'td' is the value for each column.

Add the header and all rows to Pandas data frame.

### Data type
By default all column data type in the Dataframe will be Object (string).
Inspect columns and cast each column into correct data type:
1. id               : int
2. terrestrial_date : datetime
3. sol              : int
4. ls               : int
5. month            : int
6. min_temp         : float
7. pressure         : float

### Analysis
1. Months - Unique values in the month column
2. Number of martian days - Unique values in the sol column
3. Average minimum temperature - pandas groupby month and use the mean function.
4. Plot the average minimum temperature and sort the columns to figure out coldes and hottest
5. Plot the average pressure and sort columns to figure out min and max pressure months.
6. Plotting daily minimum temperature for all the sols, we can visually see a pattern with minimum and maximum daily temperature. If we note the difference between troughs or peaks the number of days in one martian year is 690.
7. Save all data in dataframe to a CSV
