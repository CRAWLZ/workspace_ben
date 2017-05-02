
# Scraping Methods for CRAWLZ

These different methods implement different ways of collecting data from Facebook, Google, Foursquare and SGPBusiness, and is used for the CRAWLZ project found over at https://github.com/crawlzstage/infra

The CRAWLZ project uses the Facebook Graph API, the Foursquare API, and Google Places API mainly for retrieving data. The LinkedIn and SGPBusiness scrapers are prototypical scrapers that was implemented at the start but was not used later on for the final product.

## Install Dependencies

First, clone the repo.
Then run this in the terminal


`pip install -r requirements.txt`

## SGPBusiness Scraper and breaking reCAPTCHA

The SGPBusiness Scraper is not used in the final product of CRAWLZ, but is more of a proof of concept for beating Google's reCAPTCHA. The idea of breaking Google's reCAPTCHA through its audio challenge came from another Github repository: https://github.com/eastee/rebreakcaptcha

The SGPBusiness uses Scrapy to scrape through the website. Scrapy can be installed via:

`pip install Scrapy`

It will be installed when installing the other dependencies as well. In order to run the scraper for SGPBusiness, navigate to the FYP/sgpbusiness/sgpbusiness_scraper folder then run this command:

`scrapy crawl sgpbusiness`

If you want an output file, run this command:

`scrapy crawl sgpbusiness -o sgpbusiness_output.jl`


## LinkedIn initial scraper

The LinkedIn initial scraper is not used in the main project and is only listed here as a proof-of-concept, however due to LinkedIn's strict policy of web crawlers, we did not use it in the end for the main project. It is recommended not to run the program for a long time to prevent any legal issues. 

You can try running the LinkedIn prototype scraper by navigating to the linkedin_scraper folder then running linkedin_initial.py. The response returned by linkedin will be responses consisting of 200 and 999. 200 means it managed to retrieve company data, 999 means it failed. Use Ctrl-C in the middle of the program run to retrieve an output file named 'data.json'


