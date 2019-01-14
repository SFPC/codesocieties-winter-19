# Day 4: Building Nets for Floating Data

Building Nets for Floating Data is a one-session class on scraping information from websites, including text, images, and source code. We will talk about potential uses of large datasets, look at examples of artworks that use scraping as their informational backbone, and survey the ecosystem of online information gathering at large.

We will discuss popular alternatives to scraping, from APIs (online communication portals that serve data from organizations) to pre-gathered datasets uploaded to Github (for machine learning and other tasks). We will talk about this type of packaged data, as well as bias that is so often contained within.

By web-scraping without going through an organizational or corporate medium, we are able to make datasets that are more flexible, personal, and just. We are able to pull information from websites, organizations, or individuals that do not have the overhead to provide an official access point, as well as to build systems that help push back against the social, racial, economic, and other biases so often contained in large datasets. We may also be able to circumnavigate political or corporate ‘locks’ on data, scraping information that may be hidden.

After getting a handle on the landscape of web-scraping at large, we will talk about the type of websites that are easy to work with and look over example code in Python 3 and Node.js. By the end of the class, everyone will have a working web-scraper on their machine to use in the future.

+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

On Day 4 of Code Societies, we were joined by Everest Pipkin, a multimedia artist who works in software: games, bots, and beyond, as well as tactile physical mediums - for a conversation on the ethics of web scraping followed by a skillshare on how to get a scraper running on our local machines. Everest started this session by giving an overview of the three methodologies for getting data from the web as well as the advantages and shortcomings of each of them.

We started with the alternatives: Application Program Interfaces (APIs) and pre-compiled datasets. APIs are essentially user interfaces for our computers. They provide easier access points for code running on your machine to fetch data and perform operations based on the data that is returned from the access point. APIs can be incredibly useful because they often allow users to access hidden metrics and perform mass operations that aren't possible in a GUI focused internet. Everest said that they avoid using APIs as much as possible because they are often corporate, and like most corporate projects they likely have an agenda. It is important to consider what kind of data these corporations want you, a developer, a technologist, to have access to. Conversely, what might they be hiding or obscuring from their API? Is it free? If it is, then consider that you may be the product. Your usage of the API might be generating data that Major Corporation finds useful, profitable. Do you know where their data is sourced from? Is it ethical in whatever ways are most significant to you? Will your using their product make you an implicit supportor of their mission?

The other alternative, precompiled datasets, which are often hosted on sites like Github or institutional datastores created for both academic and nonacademic research, share many of the same shortcomings as APIs. Precompiled datasets are commonly used to fed machine learning models and deepening on the methodologies used to coallesece them feed different


    - when this data is fed into an MLM algorithm it can magnify and reproduce some of the problems that already exist
        - massive reprecussions in the day to day, influence voter turnout
- apis dont reflect space on the internet that do not have teh personal resources or coing knowledge to provide easy access: marginal communities that cannot publicize themselves
- precompiled datasets also fail to represent the margins
- problems with scraping:
    - consent?
    - bias? internet sources are deeply biased
    - not as clean or structured as other options
    - probably have to learn reg-ex
    - one time operation w/ data downloaded to your comp. if you want to date info, you'll need to scrape again
    - sometimes scrambling and anonymizing data can work to bury hateful language and bias, turning it from an obvious outlier to a hidden data point
- webscraping gives you power 
    - scrap info from coporations or governmental agencies
    - carefully seek sources from those often not represented in positions of power
    - see where your info is coming from and avoid or remove spaces that are deeply horrible 
- scraping is prefect for data that is ungather, under-respected, or generally lacks the resources to be bundled into a set, it is "floating"
- we as people are looking for the poetic edges of the internet
- building your own data set lets you have hyper-specific control for tone, vibe, content, language, and poetics of that spacke. making a generative work is 95% having the right material to work with

We then moved on to talk more indepth about web scraping. What is it and why would we want to use it? Web scraping is a code based methodology for pulling data off websites without having to go through an offical access point like an Application Program Interface (API).



# Build Yourself a Web Scraper

**These instructions are specific to macOS.**

Before we begin you will need to handle a few installations.
- pip, the offical python package manager
- BeautifulSoup4, a web-scraping library
- requests, a library for making HTTP requests

```python
# you will need admin privledges to your machine
sudo easy_install pip
pip install BeautifulSoup4
pip install requests
```

Create a file in your directory of choice called `scraper.py`, and in it copy and paste the code below. start by sending a request to 

```python
import requests
page = requests.get("http://ppg.thebrownhouse.org/")s

# this will print out the status code onto your console
# a successful request will output 200
print(page)
```

```python
import requests
page = requests.get("http://ppg.thebrownhouse.org/")
# now change page to page.content
print(page.content)
```


```python
# now use beautiful soup
from bs4 import BeautifulSoup, SoupStrainer
import requests
page = requests.get("http://ppg.thebrownhouse.org/")
soup = BeautifulSoup(page.content, 'html.parser')
print(soup.prettify())

```

```python
from bs4 import BeautifulSoup, SoupStrainer
import requests
page = requests.get("http://ppg.thebrownhouse.org/")
soup = BeautifulSoup(page.content, 'html.parser')

# get a list of all the child elements on the page
print(list(soup.children))
```