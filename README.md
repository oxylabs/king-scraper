# King Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [King Scraper](https://oxylabs.io/products/scraper-api/ecommerce/king?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an King website effortlessly. This brief guide showcases how King Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get King results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of King page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://king.ro/vinuri-bag-in-box/'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/king-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\n<!DOCTYPE html>\n<html \n lang=\"ro\" dir=\"ltr\">\n<head>\n                <title>Vin Bag in Box pret de l ... </html>",
      "created_at": "2024-02-20 12:31:35",
      "updated_at": "2024-02-20 12:31:37",
      "page": 1,
      "url": "https://king.ro/vinuri-bag-in-box/",
      "job_id": "7165684410686126082",
      "status_code": 200
    }
  ]
}
```
With our King Scraper, you can seamlessly pull public data from any accessible King website. Gather all necessary product details, including cost, feedback, or definition, to scrutinize the industry and stay ahead in the race. If you run into any troubles, reach out to our support crew through live chat or drop us an email at hello@oxylabs.io.