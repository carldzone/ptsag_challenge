# ptsag_challenge
If you want to run it on your local machine, follow these steps steps on your local Linux machine

### Create your virtual environment first
```
python3 -m venv venv
```
### Activate your venv
```
source venv/bin/activate
```
### Install requirements.txt
```
pip install -r requirements.txt
```
### Install necessary packages such as Playwright
```
playwright install
```

## If you want to run the crawler to produce your own output. Make sure you are in the scraping_challenge folder
```
cd scraping_challenge
scrapy crawl scraping -O ScrapingSpider_`date +\%Y\%m\%d_\%H\%M\%S`.json
```
## If you want an .xlsx output:
Go to settings.py and uncomment this line. Make sure to uncomment it out after using it so that the settings won't get messed up
```
## For xlsx output 
FEED_EXPORTERS = {
    'xlsx': 'scrapy_xlsx.XlsxItemExporter',
}
```
And the run this line of code
```
scrapy crawl scraping -O ScrapingSpider_`date +\%Y\%m\%d_\%H\%M\%S`.xlsx
```