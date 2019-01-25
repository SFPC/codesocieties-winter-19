---
title: "Day 4: Building Nets for Floating Data"
author: written by Mimi Doan
---

_Building Nets for Floating Data is a one-session class on scraping information from websites, including text, images, and source code. We will talk about potential uses of large datasets, look at examples of artworks that use scraping as their informational backbone, and survey the ecosystem of online information gathering at large._

[Link to Full Syllabus](https://docs.google.com/document/d/1I1kM6lD8zPUvxakIujNj0HeUdmYFVAwnrt0s18BvMMQ/edit)

#

On Day 4 of Code Societies, we were joined by Everest Pipkin, a multimedia artist who works in software: games, bots, and beyond, as well as tactile physical mediums - for a conversation on the ethics of web scraping followed by a skillshare on how to get a scraper running on our local machines. Everest started this session by giving an overview of the three methodologies for getting data from the web as well as the advantages and shortcomings of each of them.

We started with the alternatives: Application Program Interfaces (APIs) and pre-compiled datasets. APIs are essentially user interfaces for our computers. They provide easier access points for code running on your machine to fetch data and perform operations based on the data that is returned from the access point. APIs can be incredibly useful because they often allow users to access hidden metrics and perform mass operations that aren't possible in a GUI focused internet. Everest said that they avoid using APIs as much as possible because they are often corporate and like most corporate projects they likely have an agenda.

It is important to consider what kind of data these corporations want you, a developer, a technologist,  to have access to. Conversely, what might they be hiding or obscuring from their API? Is it free? If it is, then consider that you might be the product. Your usage of the API might be generating data that Major Corporation finds useful, profitable. Do you know where their data is sourced from? Is it ethical in whatever ways are most significant to you? Will your using their product make you an implicit supporter of their mission?

![Everest Pipkin on why artists should consider scraping]({{
  "/assets/everest-pipkin.JPG" | relative_url }})

The other alternative, precompiled datasets, which are often hosted on sites like Github or institutional datastores created for both academic and nonacademic research, share many of the same shortcomings as APIs. Precompiled datasets are commonly used to feed machine learning models and depending on the methodologies used to coalesce the data, emulate different sets of biases. Biased data creates biased machine learning models which magnify and reproduce problems that already exist.

Biased data and the products created from them have massive repercussions on our experiences of the everyday. It can influence voter turnout; it can be used to justify violence against communities that are already hyper-policed. Machine learning will not save us from our subjectivity. Furthermore, APIs and precompiled datasets rarely reflect space online spaces that do not have the personal resources or the technological skillsets to quantify and represent themselves in these ways. They do not reflect communities on the margins that do not have a representation on the internet.

We then moved on to talk more in-depth about web scraping. What is it and why would we want to use it? Web scraping is a code based methodology for pulling data off websites without having to go through official portals or access points. Web scraping gives us, independent researchers, technologists, artists,
the ability to bypass corporations and governmental agencies in our pursuit of data and information. We can be more careful, more tactical in where we choose to source from and who we seek to represent in our datasets. "Scraping is perfect for data that is ungathered, under-respected, or generally lacks the resources to be bundled into a set; data that is "floating."

Web scraping also gives you the power to punch up, to bypass the walled gardens of [government agencies](https://www.nytimes.com/2017/03/06/science/donald-trump-data-rescue-science.html) and big corporations that do not want to give you easy ways of accessing their data. We specifically talked about Sam Lavigne's project from June of 2018 in which they scraped LinkedIn for the profiles of everyone who worked for ICE. Sam hosted the data on Github and wrote a Medium article about this project and within 24 hours both sites had removed his work under the guise that they do not promote Doxxing on their platforms. You can find an archived version of the article [here](https://archive.fo/0aYO3) and an archived version of the CSV [here](https://archive.fo/VhOLb).

![Everest Pipkin on navigating consent]({{
  "/assets/everest-pipkin-2.JPG" | relative_url }})

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

![Everest Pipkin showing artwork they made with old cursors]({{
  "/assets/everest-pipkin-3.JPG" | relative_url }})

![Everest Pipkin showing an application they recently made]({{
  "/assets/everest-pipkin-4.JPG" | relative_url }})

## Build Yourself a Web Scraper

**These instructions are specific to macOS,** but should also work on most UNIX/LINUX machines.

If you're new to programming, consider going through our [day 2 blog post, Computational Methods of Code Societies,](http://sfpc.io/codesocieties-winter-19/2019/01/08/computational-methods-of-code-societies.html) before beginning for an overview of terminal and command line basics. Our final product will be a python file that outputs the contents of `http://ppg.thebrownhouse.org/`, a hobbyist's power paragliding website with an easily traversible table structure.


Before we begin you will need to handle a few installations.

- `pip`, the offical python package manager
- `python3`, the lastest version of python
- `BeautifulSoup4`, a web-scraping library
- `requests`, a library for making HTTP requests

Follow these instructions to [install python3](https://wsvincent.com/install-python3-mac/). After installing python3, check if pip is installed by running `pip --version` in your terminal. If you see anything that's not an error messgae, you're good to skip the `sudo easy_install pip` step.

Now, run these commands in your terminal to install pip, BeautifulSoup, and requests before moving on.

```python
# you will need admin privledges to your machine
sudo easy_install pip
pip install BeautifulSoup4
pip install requests
```

Create a file in your directory of choice called `scraper.py`, and in it copy and paste the code below. This code will send an [HTTP GET](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol#Request_methods) request to `http://ppg.thebrownhouse.org/`, use the BeautifulSoup library to parse through the site, and then print the page contents to your terminal.

```python
# import the required python libraries into our file
from bs4 import BeautifulSoup, SoupStrainer
import requests

# send GET request
page = requests.get("http://ppg.thebrownhouse.org/")

# this function returns the page content and stores it in
# a variable called soup
soup = BeautifulSoup(page.content, 'html.parser')

# print our soup to the console
print(soup.prettify())
```

Run your web scraper by typing `python3 scraper.py` into your terminal. Make sure that you do this in the same directory that the file is in.

Congratulations! You now have a web scrapper running on your local machine. Checkout [BeautifulSoup's](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) documentation for more ways to use the library.
