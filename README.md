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
