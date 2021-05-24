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
<b> Code for requesing data from Website </b>
## The BeautifulSoup Object
  When we printed out all of that HTML from our request, it seemed pretty long and messy. How could we pull out the relevant information from that long string? <br>
  BeautifulSoup is a Python library that makes it easy for us to traverse an HTML page and pull out the parts we’re interested in. We can import it by using the line:
<b>from bs4 import BeautifulSoup</b>
Then, all we have to do is convert the <b>HTML document to a BeautifulSoup object!</b><br>
  <b>soup = BeautifulSoup("rainbow.html", "html.parser")</b>
    
## Object Types
BeautifulSoup breaks the HTML page into several types of objects.
1. Tags
2. NavigableStrings
### Tags
A Tag corresponds to an HTML Tag in the original document. These lines of code:
<br>
"soup = BeautifulSoup('<div id="example">An example div</div><p>An example p tag</p>')"
print(soup.div)
### NavigableStrings
NavigableStrings are the pieces of text that are in the HTML tags on the page. You can get the string inside of the tag by calling .string:
<br>
<b> Code Of Taking out String from Tags </b>
## Navigating by Tags
  To navigate through a tree, we can call the tag names themselves. Imagine we have an HTML page that has different tags like (h1, p, li, ul, ol) <br> If we made a soup object out of this HTML page, we have seen that we can get the first h1 element by calling:

print(soup.h1)<br> We can get the children of a tag by accessing the .children attribute:
<br>
for child in soup.ul.children:
    print(child)<br>
  
  ## Website Structure
When we’re telling our Python script what HTML tags to grab, we need to know the structure of the website and what we’re looking for.
Many browsers, including Chrome, Firefox, and Safari, have Dev Tools that help you inspect a webpage and see what HTML elements it is composed of.  
First learn this,
<a href="https://www.codecademy.com/articles/use-devtools">How To Use DevTools</a>
## Find All
If we want to find all of the occurrences of a tag, instead of just the first one, we can use .find_all().
This function can take in just the name of a tag and returns a list of all occurrences of that tag.

print(soup.find_all("h1"))
