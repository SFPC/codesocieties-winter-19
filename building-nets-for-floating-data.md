# Day 4: Building Nets for Floating Data

Building Nets for Floating Data is a one-session class on scraping information from websites, including text, images, and source code. We will talk about potential uses of large datasets, look at examples of artworks that use scraping as their informational backbone, and survey the ecosystem of online information gathering at large.

We will discuss popular alternatives to scraping, from APIs (online communication portals that serve data from organizations) to pre-gathered datasets uploaded to Github (for machine learning and other tasks). We will talk about this type of packaged data, as well as bias that is so often contained within.

By web-scraping without going through an organizational or corporate medium, we are able to make datasets that are more flexible, personal, and just. We are able to pull information from websites, organizations, or individuals that do not have the overhead to provide an official access point, as well as to build systems that help push back against the social, racial, economic, and other biases so often contained in large datasets. We may also be able to circumnavigate political or corporate ‘locks’ on data, scraping information that may be hidden.

After getting a handle on the landscape of web-scraping at large, we will talk about the type of websites that are easy to work with and look over example code in Python 3 and Node.js. By the end of the class, everyone will have a working web-scraper on their machine to use in the future.

+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

On Day 4 of Code Societies, we were joined by Everest Pipkin, a multimedia artist who works in software: games, bots, and beyond, as well as tactile physical mediums - for a conversation on the ethics of web scraping followed by a skillshare on how to get a scraper running on our local machines. Everest started this session by giving an overview of the three methodologies for getting data from the web as well as the advantages and shortcomings of each of them.

We started with the alternatives: Application Program Interfaces (APIs) and pre-compiled datasets. APIs are essentially user interfaces for our computers. They provide easier access points for code running on your machine to fetch data and perform operations based on the data that is returned from the access point. APIs can be incredibly useful because they often allow users to access hidden metrics and perform mass operations that aren't possible in a GUI focused internet. Everest said that they avoid using APIs as much as possible because they are often corporate and like most corporate projects they likely have an agenda. 

It is important to consider what kind of data these corporations want you, a developer, a technologist,  to have access to. Conversely, what might they be hiding or obscuring from their API? Is it free? If it is, then consider that you might be the product. Your usage of the API might be generating data that Major Corporation finds useful, profitable. Do you know where their data is sourced from? Is it ethical in whatever ways are most significant to you? Will your using their product make you an implicit supporter of their mission?

The other alternative, precompiled datasets, which are often hosted on sites like Github or institutional datastores created for both academic and nonacademic research, share many of the same shortcomings as APIs. Precompiled datasets are commonly used to fed machine learning models and depending on the methodologies used to coalesce the data, emulate different sets of biases. Biased data creates biased machine learning models which magnify and reproduce problems that already exist.

Biased data and the products created from them have massive repercussions on our experiences of the everyday. It can influence voter turnout; it can be used to justify violence against communities that are already hyper-policed. Machine learning will not save us from our subjectivity. Furthermore, APIs and precompiled datasets don't often reflect space on the internet that do not have the personal resources or the technological skillsets to create them. They do not provide access to communities on the margins that cannot publicize themselves. 

We then moved on to talk more in-depth about web scraping. What is it and why would we want to use it? Web scraping is a code based methodology for pulling data off websites without having to go through official portals or access points. Web scraping gives us, independent researchers, technologists, artists,
the ability to bypass corporations and governmental agencies in our pursuit of data and information. We can be more careful, more tactical in where we choose to source from and who we seek to represent in our datasets. "Scraping is perfect for data that is ungathered, under-respected, or generally lacks the resources to be bundled into a set; data that is "floating."

Web scraping also gives you the power to punch up, to bypass the walled gardens of [government agencies](https://www.nytimes.com/2017/03/06/science/donald-trump-data-rescue-science.html) and big corporations that do not want to give you easy ways of accessing their data. We specifically talked about Sam Lavigne's project from June of 2018 in which they scraped LinkedIn for the profiles of everyone who worked for ICE. Sam hosted the data on Github and wrote a Medium article about this project and within 24 hours both sites had removed his work under the guise that they do not promote Doxxing on their platforms. You can find an archived version of the article [here](https://archive.fo/0aYO3) and an archived version of the CSV [here](https://archive.fo/VhOLb).

Despite its advantages, web scraping is far from a perfect technology. In sourcing from the internet, the data collected will be biased - it will have bias regardless of how or where it is sourced from, but we can be selective in avoiding the most horrible and violent corners of the internet. Web scraping is also a onetime operation - the only way to get dated information is to scrape again and again. Scraped data is usually not as clean as data coming from APIs or precompiled sets and it might take some additional massaging with python and learning of [Reg-Ex](https://regexr.com/) before the data is usable. 

These are a few of the disadvantages of exclusively sourcing through web scrapping, but the most central concern arises when considering the question of how we hold conversations about consent when scraping from the web? Everest said their current solution for this issue is to use Creative Commons no-attribution work whenever possible, but to attribute liberally anyway, and to always be ready to pull something off if someone asks, but there is no One Right Answer.

Everest went on to show us examples of work made by:

**_web scraping_** 
- [Shiv Integer](http://www.plummerfernandez.com/Shiv-Integer) -- 3d model Thingiverse bot, M Plummer-Fernandez and Julien Deswaef
- [The Seeker](https://github.com/thricedotted/theseeker) -- A generated poetry book from WikiHow by Li Zi
- [Suns from Sunsets from Flickr](http://www.penelopeumbrico.net/index.php/project/suns/) & [Everyone’s Photos Any License](http://www.penelopeumbrico.net/index.php/project/flickr-moons/) -- Flickr collections from Penelope Umbrico


**_coalescing data by hand_**
- [Mosaic Virus](http://annaridler.com/mosaic-virus/) -- Machine-learning generated Tulips by Anna Ridler
- [VR 3](http://www.pippinbarr.com/2017/03/29/v-r-3/) -- A museum of all the water on the Unity Store by Pippin Barr

## Build Yourself a Web Scraper

**These instructions are specific to macOS.**

Before we begin you will need to handle a few installations.
- `pip`, the offical python package manager
- `BeautifulSoup4`, a web-scraping library
- `requests`, a library for making HTTP requests

```python
# you will need admin privledges to your machine
sudo easy_install pip
pip install BeautifulSoup4
pip install requests
```

Create a file in your directory of choice called `scraper.py`, and in it copy and paste the code below. We'll start by sending a GET request to `http://ppg.thebrownhouse.org/`, a hobbiest's power paragliding website with an easily traversible table structure.

```python
import requests
page = requests.get("http://ppg.thebrownhouse.org/")

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
# now use beautiful soup to print a prettified version of the site
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

Congratulations! You now have a web scrapper running on your local machine. Checkout [BeautifulSoup's](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) documentation for more ways to use the library.