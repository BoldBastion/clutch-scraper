[Clutch Scraper](https://apify.com/alizarin_refrigerator-owner/clutch-scraper?fpr=data)

# Clutch.co Agency Scraper

Scrape B2B agency profiles from Clutch.co. Extract company info, reviews, ratings, pricing, services, clients, and portfolios. Perfect for B2B lead generation and competitive analysis. Built by John Rippy ([https://www.linkedin.com/in/johnrippy/](https://www.linkedin.com/in/johnrippy/) | [https://johnrippy.link/](https://johnrippy.link/)).

---

## Quick Start

### Test with Demo Mode (free, no API key needed)

```
{
  "demoMode": true,
  "searchQuery": "digital marketing agency"
}
```

### Run with real data

```
{
  "demoMode": false,
  "searchQuery": "digital marketing agency",
  "maxResults": 50,
  "includeReviews": true,
  "webhookPlatform": "custom"
}
```

---

## Input Parameters

| Parameter | Type | Default | Required | Description |
| --- | --- | --- | --- | --- |
| `demoMode` | boolean | `true` | No | Run with sample data without making API calls. Great for testing the actor. |
| `searchQuery` | string | - | No | Search term (e.g., 'web development', 'digital marketing', 'SEO agency'). |
| `location` | string | - | No | Filter by location (e.g., 'United States', 'New York', 'London'). |
| `category` | string | - | No | Filter by service category. |
| `minRating` | number | - | No | Filter by minimum rating (1-5). |
| `maxResults` | integer | `50` | No | Maximum number of agencies to scrape. |
| `includeReviews` | boolean | `true` | No | Scrape detailed reviews for each agency (slower but more data). |
| `webhookUrl` | string | - | No | URL to POST results when scraping completes (Zapier, Make, n8n, custom endpoint) |
| `webhookPlatform` | string | `"custom"` | No | Platform-specific payload formatting |
| `webhookHeaders` | object | - | No | Custom HTTP headers to send with webhook (JSON object) |

---

## Pricing

This actor uses **pay-per-event** billing:

| Event | Description | Price |
| --- | --- | --- |
| Agency Scraped | Each agency profile scraped from Clutch.co | $0.05 |

**Demo mode is free** -- no charges for sample data.

---

## Troubleshooting

### "API error 429" or "Rate limit"

Too many requests. Wait a minute and try again, or reduce the number of items per run.

### No results or empty dataset

Check the run log for error messages. Common causes:

- Invalid input format (check the examples above)
- The target data doesn't exist or is too small to track

### How do I test without an API key?

Enable **Demo Mode** in the input. This returns realistic sample data so you can verify the output format works for your workflow.

---

**Built by John Rippy | [Actor Arsenal](https://actorarsenal.com)**