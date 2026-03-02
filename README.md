# 法務部行政執行署拍賣公告爬蟲 (Vehicle Auction Scraper)

This script is a template for scraping vehicle (car/motorcycle) auction announcements from the Ministry of Justice Administrative Enforcement Agency.

## Status: Template Only

The actual website (https://www.tpkonsale.moj.gov.tw/Chattel) requires specific POST requests or CSS selectors that cannot be verified without browser access. This script provides the structure (BeautifulSoup + Requests) you will need.

## How to Complete

1. **Inspect the Site:** Open the URL in your browser, press F12, and check the network tab when searching for vehicles.
2. **Update the Script:**
   - If the site uses an API (XHR/Fetch), change `requests.get` to `requests.post` and include the correct payload.
   - If the site renders HTML directly, find the class names for auction items (e.g., `.auction-list`, `.title`, `.date`) and update the `soup.select()` calls in `moj_auction_scraper.py`.

## Usage

```bash
pip install requests beautifulsoup4
python moj_auction_scraper.py
```
