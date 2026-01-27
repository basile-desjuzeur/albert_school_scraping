## Robust vs Fragile Extraction

When scraping, **how you select elements matters** more than the code itself.

### Avoid fragile extraction

Fragile selectors break easily when:
- the text changes
- the page layout changes
- the website redesigns CSS classes

**Examples** of fragile strategies:
- selecting by visible text
- relying on long or random class names
- assuming fixed positions (e.g. “the 3rd div”)

```python
# Fragile: depends on visible text
soup.find("a", text="Click here")
```

# Ethics & Legality of Web Scraping

Scraping is not hacking, but it is not always allowed.
## What scraping is
- Sending HTTP requests
- Reading publicly accessible HTML
- Parsing data already sent to your browser
## What scraping is NOT
- Bypassing logins
- Avoiding paywalls
- Circumventing CAPTCHAs
- Overloading servers
- robots.txt (conceptual)

Many websites publish rules for bots at:
https://example.com/robots.txt
It may specify:
- which paths are allowed
- crawl delays
Even if not legally binding, it represents expected behavior.
## APIs vs Scraping
If a website provides an official API:
- Use the API
- Don’t scrape HTML
APIs are:
- more stable
- documented
- rate-limited clearly
- legally safer

## Good scraping practices
- Identify yourself with a User-Agent
- Use time.sleep() to limit request rate
- Scrape only what you need
- Avoid personal or sensitive data

## Static vs Dynamic scraping

For static scraping : requests + BS4 should be used
For dynamic scraping : use Selenium