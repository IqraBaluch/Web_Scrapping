# Web_Scrapping
## WEB SCRAPING WITH BEAUTIFUL SOUP
### <b>Prerequisites</b>
1. Knowlege of Python
2. Understnding of Python library Pandas
### Dataset
With the right dataset alot of exciting works can be done. Once we have interesting data we can use Python, Pandas and matplotlib to analyze or visualize the data. If the dataset is provided in scv or json file, its easy to work on it directly otherwise we have to search for dataset first.
<br> Mostly we find the dataset we are looking for, but there is no way to download it. This is where BeautifulSoup comes in handy to scrape the HTML. BeautifulSoup is used to analyze online data and bring the data in a structure, we can understand it. <br> 
## Requests
In order to get the html of the website, we need to make a request. Python ha a library "requests", that makes getting content really easy. All we have to do is to import the library and and then feed in the URL we want to GET: <br>
<b> Request Code </b>
## The BeautifulSoup Object
  When we printed out all of that HTML from our request, it seemed pretty long and messy. How could we pull out the relevant information from that long string? <br>
  BeautifulSoup is a Python library that makes it easy for us to traverse an HTML page and pull out the parts we’re interested in. We can import it by using the line:
<b>from bs4 import BeautifulSoup</b>
Then, all we have to do is convert the <b>HTML document to a BeautifulSoup object!</b><br>
  <b>soup = BeautifulSoup("rainbow.html", "html.parser")</b>
    
