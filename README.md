# Total-Wine Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Total-Wine Scraper](https://oxylabs.io/products/scraper-api/ecommerce/total-wine?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Total-Wine website effortlessly. This brief guide showcases how Total-Wine Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Total-Wine results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Total-Wine page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.totalwine.com/wine/c/c0020'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/total-wine-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\n    <!DOCTYPE html>\n    <html lang=\"en\">\n      <head profile=\"http://www.w3.org/2005/10/profile\">\n  ... </html>",
      "created_at": "2024-02-20 12:53:18",
      "updated_at": "2024-02-20 12:53:21",
      "page": 1,
      "url": "https://www.totalwine.com/wine/c/c0020",
      "job_id": "7165689874408846337",
      "status_code": 200
    }
  ]
}
```
With our Total-Wine Scraper, you can easily harvest public data from any Total-Wine webpage. Gather necessary wine product details, including cost, customer evaluations, or wine descriptions, to evaluate your wine market and maintain an edge over your competition. If you require assistance, our support team is readily available via live chat or you can email us at hello@oxylabs.io.