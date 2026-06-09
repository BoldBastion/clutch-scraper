[Clutch Scraper](https://apify.com/automation-lab/clutch-scraper?fpr=data)

## What does Clutch.co Scraper do?

**Clutch.co Scraper** extracts B2B service provider data from [Clutch.co](https://clutch.co), the leading platform for finding and comparing business service providers. Paste any category or search URL and get structured company data including **ratings, reviews, contact details, hourly rates, and service breakdowns** -- all without an API key or login.

The easiest way to try it is to click **Start** with the prefilled input -- it will scrape 10 IT service companies in under 30 seconds.

Unlike the $40/month competitor, this actor uses **pay-per-result pricing** -- you only pay for what you scrape. Extract 1,000 companies for just $5.

## Who is Clutch.co Scraper for?

**Sales & Business Development teams** looking for qualified B2B leads:

- Build prospect lists of verified service providers in any category
- Filter by location, company size, hourly rate, and project budget
- Export contact details and company profiles for outreach campaigns

**Market researchers & analysts** tracking the B2B services landscape:

- Benchmark competitors across 1,100+ service categories
- Analyze pricing trends, ratings distributions, and market concentration
- Monitor new entrants and shifts in category rankings

**Procurement & sourcing teams** evaluating potential vendors:

- Compare service providers side-by-side with standardized data
- Verify company credentials, review counts, and verification status
- Build shortlists based on objective criteria (ratings, reviews, size)

**Recruitment agencies** identifying companies that may need staffing:

- Find growing companies by employee range and service expansion
- Target firms in specific locations for regional recruiting efforts

## Why use Clutch.co Scraper?

- **Pay per result, no subscription** -- unlike the $40/month competitor, pay only for what you scrape
- **Rich, structured data** -- company name, rating, reviews, location, hourly rate, project size, employees, phone, services, and more
- **80 companies per page** -- Clutch shows dense listings, so you get lots of data fast
- **Handles Cloudflare protection** -- uses residential proxy and Playwright to bypass anti-bot measures
- **Pagination support** -- automatically follows page links to scrape entire categories
- **No API key or login required** -- just paste a Clutch.co URL and go
- **Export to JSON, CSV, Excel** -- download results in any format from the Apify platform
- **Schedule and automate** -- set up recurring scrapes to monitor changes over time
- **API access** -- integrate with 5,000+ apps via Zapier, Make, and the Apify API

## What data can you extract from Clutch.co?

Each company listing includes the following fields:

| Field | Type | Example |
| --- | --- | --- |
| companyName | string | "SmartSites" |
| rating | number | 4.9 |
| reviewCount | number | 351 |
| location | string | "Paramus, NJ" |
| minProjectSize | string | "$1,000+" |
| hourlyRate | string | "$100 - $149 / hr" |
| employees | string | "250 - 999" |
| phone | string | "2018706000" |
| tagline | string | "SmartSites is a digital marketing..." |
| clutchUrl | string | "[https://clutch.co/profile/smartsites](https://clutch.co/profile/smartsites)" |
| services | string[] | ["SEO", "PPC", "Advertising"] |
| isVerified | boolean | true |
| isSponsored | boolean | true |

## How much does it cost to scrape Clutch.co?

This actor uses **pay-per-event** pricing -- you pay only for what you scrape. No monthly subscription. All platform costs are **included**.

|  | Free | Starter ($29/mo) | Scale ($199/mo) | Business ($999/mo) |
| --- | --- | --- | --- | --- |
| **Per company** | $0.00575 | $0.005 | $0.0039 | $0.003 |
| **100 companies** | $0.585 | $0.51 | $0.40 | $0.31 |
| **1,000 companies** | $5.76 | $5.01 | $3.91 | $3.01 |

A one-time **$0.01 start fee** is charged per run.

Higher-tier plans get additional volume discounts (up to 72% off at Diamond tier).

**Real-world cost examples:**

| Query | Results | Duration | Cost (Free tier) |
| --- | --- | --- | --- |
| IT services (1 page) | 10 companies | ~30s | ~$0.07 |
| SEO agencies (2 pages) | 160 companies | ~55s | ~$0.93 |
| Web developers (2 pages) | 100 companies | ~37s | ~$0.59 |

With the **free plan** ($5 credit), you can scrape approximately **850 companies** at no cost.

## How to scrape Clutch.co company data

1. Go to the [Clutch.co Scraper](https://apify.com/automation-lab/clutch-scraper) page on Apify Store.
2. Click **Start** to use the prefilled input, or customize the search URL.
3. To find your search URL, browse [Clutch.co](https://clutch.co) categories and copy the URL from your browser.
4. Set the **Max companies** limit to control how many results you want.
5. Click **Start** and wait for the run to complete.
6. Download your data in JSON, CSV, or Excel format from the **Dataset** tab.

**Example input for IT services:**

```
{
    "searchUrl": "https://clutch.co/it-services",
    "maxResults": 50
}
```

**Example input for digital marketing agencies in New York:**

```
{
    "searchUrl": "https://clutch.co/agencies/digital-marketing/new-york",
    "maxResults": 100
}
```

## Input parameters

| Parameter | Type | Default | Description |
| --- | --- | --- | --- |
| searchUrl | string | *required* | Clutch.co category, search, or location URL |
| maxResults | integer | 100 | Maximum number of companies to scrape. Set to 0 for unlimited. |
| scrapeDetails | boolean | false | Visit each company profile page for richer data (slower) |

## Output example

```
{
    "companyName": "SmartSites",
    "rating": 4.9,
    "reviewCount": 351,
    "location": "Paramus, NJ",
    "minProjectSize": "$1,000+",
    "hourlyRate": "$100 - $149 / hr",
    "employees": "250 - 999",
    "phone": "2018706000",
    "tagline": "SmartSites is a digital marketing agency specializing in SEO, PPC, and website development services...",
    "description": null,
    "website": null,
    "clutchUrl": "https://clutch.co/profile/smartsites",
    "services": [
        "Search Engine Optimization",
        "Pay Per Click",
        "Advertising",
        "Social Media Marketing"
    ],
    "focusAreas": null,
    "founded": null,
    "isVerified": true,
    "isSponsored": true
}
```

## Tips for best results

- **Start small** -- use the prefilled input (10 companies) for your first run to verify the data matches your needs.
- **Use specific category URLs** -- Clutch has 1,100+ categories. Browse Clutch.co to find the most relevant one, then paste that URL.
- **Location filtering** -- Clutch supports location-filtered URLs like `https://clutch.co/agencies/seo/san-francisco`. Use these for geo-targeted results.
- **Schedule regular runs** -- company ratings, reviews, and rankings change frequently. Set up weekly or monthly scrapes to track trends.
- **Combine with other data** -- use the `clutchUrl` field to cross-reference with other sources, or the `phone` field for outreach.
- **Monitor costs** -- each page yields ~80 companies. A 100-company scrape costs about $0.51 on the Starter plan.

## Integrations

- **Clutch.co Scraper --> Google Sheets** -- automatically populate a spreadsheet with B2B provider data for team sharing and analysis. Set up a scheduled actor run with a Google Sheets webhook.
- **Clutch.co Scraper --> Slack** -- get notified when new high-rated companies appear in your target category. Use a Zapier integration to filter by rating > 4.5 and post to your sales channel.
- **Clutch.co Scraper --> CRM (HubSpot, Salesforce)** -- import company data as leads with ratings, services, and contact details pre-filled. Connect via Make or Zapier.
- **Scheduled monitoring** -- run weekly scrapes of competitor categories to track rating changes, new entrants, and pricing shifts.
- **Webhooks** -- trigger downstream processing (lead scoring, email sequences) when new data is available.

## Using the Apify API

You can access Clutch.co Scraper programmatically using the Apify API.

### Node.js

```
import { ApifyClient } from 'apify-client';

const client = new ApifyClient({ token: 'YOUR_APIFY_TOKEN' });
const run = await client.actor('automation-lab/clutch-scraper').call({
    searchUrl: 'https://clutch.co/it-services',
    maxResults: 50,
});
const { items } = await client.dataset(run.defaultDatasetId).listItems();
console.log(items);
```

### Python

```
from apify_client import ApifyClient

client = ApifyClient('YOUR_APIFY_TOKEN')
run = client.actor('automation-lab/clutch-scraper').call(run_input={
    'searchUrl': 'https://clutch.co/it-services',
    'maxResults': 50,
})
items = client.dataset(run['defaultDatasetId']).list_items().items
print(items)
```

### cURL

```
curl -X POST "https://api.apify.com/v2/acts/automation-lab~clutch-scraper/runs?token=YOUR_APIFY_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"searchUrl": "https://clutch.co/it-services", "maxResults": 50}'
```

## Use with AI agents via MCP

Clutch.co Scraper is available as a tool for AI assistants that support the [Model Context Protocol (MCP)](https://docs.apify.com/platform/integrations/mcp).

Add the Apify MCP server to your AI client -- this gives you access to all Apify actors, including this one:

### Setup for Claude Code

```
$claude mcp add --transport http apify "https://mcp.apify.com?tools=automation-lab/clutch-scraper"
```

### Setup for Claude Desktop, Cursor, or VS Code

Add this to your MCP config file:

```
{
    "mcpServers": {
        "apify": {
            "url": "https://mcp.apify.com?tools=automation-lab/clutch-scraper"
        }
    }
}
```

Your AI assistant will use OAuth to authenticate with your Apify account on first use.

### Example prompts

Once connected, try asking your AI assistant:

- "Use automation-lab/clutch-scraper to find the top 20 IT consulting firms in New York with ratings above 4.5"
- "Scrape all SEO agencies from Clutch.co and create a comparison spreadsheet with ratings, prices, and employee counts"
- "Find B2B software development companies in Europe on Clutch.co and rank them by review count"

Learn more in the [Apify MCP documentation](https://docs.apify.com/platform/integrations/mcp).

## Is it legal to scrape Clutch.co?

Scraping publicly available data from Clutch.co is generally legal. This actor only extracts information that is publicly visible to any visitor of the website -- company names, ratings, reviews, and contact details that businesses have chosen to publish.

We follow ethical scraping practices:

- Only public data is collected (no login required)
- Requests are rate-limited to avoid overloading servers
- Data is used for legitimate business purposes (lead generation, market research, procurement)

For GDPR compliance, ensure you have a lawful basis for processing any personal data (such as phone numbers) in your jurisdiction.

## FAQ

**How fast is the Clutch.co Scraper?**
Each page of results (~80 companies) takes about 10-15 seconds to scrape, including Cloudflare challenge handling. A typical 100-company scrape finishes in under 60 seconds.

**How does this compare to the official Clutch.co API?**
Clutch.co does not offer a public API. This scraper extracts the same data visible on the website and structures it as clean JSON for programmatic use.

**Why are some fields null (website, focusAreas, founded)?**
These fields are only available on individual company profile pages, not on listing pages. Enable the "Scrape company details" option to visit each profile and fill in these fields (this makes runs slower).

**Why am I getting fewer results than expected?**
Some Clutch.co categories have fewer listings than the maxResults you set. The scraper will return all available results up to your limit. Also check that your URL is a valid Clutch.co category or search page.

**Why did my run fail with a timeout?**
Cloudflare protection can occasionally block requests even with residential proxy. Try running again -- the proxy will use a different IP address. If failures persist, reduce maxResults.

## Who is it for

- **Marketers and sales teams** building targeted outreach lists of B2B service providers, filtered by category, location, size, and budget range.
- **Market researchers and competitive analysts** tracking the B2B services landscape -- benchmarking ratings, pricing trends, and category growth across 1,100+ Clutch categories.
- **Procurement and sourcing professionals** evaluating vendors with standardized, structured data instead of manual comparison.
- **Recruitment agencies** identifying fast-growing companies by employee count and service expansion to target for staffing opportunities.
- **Data-driven consultants** who need clean, exportable datasets of verified service providers for client deliverables and strategy reports.

## Pricing

This actor uses pay-per-event pricing. See the Pricing tab on Apify Store for current rates.

## API usage

You can start Clutch.co Scraper programmatically via the [Apify API](https://docs.apify.com/api/v2). Replace `YOUR_APIFY_TOKEN` with your API token from [Apify Console](https://console.apify.com/account#/integrations).

**Start a run:**

```
curl -X POST "https://api.apify.com/v2/acts/7n2eZwPoggPMbSskf/runs?token=YOUR_APIFY_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"searchUrl": "https://clutch.co/it-services", "maxResults": 50}'
```

**Get dataset items from the last run:**

```
$curl "https://api.apify.com/v2/acts/7n2eZwPoggPMbSskf/runs/last/dataset/items?token=YOUR_APIFY_TOKEN"
```

For full details, see the [Apify API reference](https://docs.apify.com/api/v2) or use the Node.js and Python client examples in the sections above.

## MCP

This actor is compatible with Model Context Protocol (MCP). Use it with AI assistants via the Apify MCP server.

## Legality

Scraping publicly available data is generally considered legal in most jurisdictions. This actor only accesses pages that are publicly visible to any website visitor -- no login, authentication, or paywall bypass is involved.

However, web scraping exists in a legal gray area that varies by country and use case. Before using scraped data, consider the following:

- **Terms of Service** -- review Clutch.co's ToS to understand their position on automated access. Compliance with site terms is your responsibility.
- **Personal data (GDPR/CCPA)** -- some extracted fields (e.g., phone numbers) may qualify as personal data. Ensure you have a lawful basis for processing and storing this information in your jurisdiction.
- **Rate limiting** -- this actor uses built-in rate limiting and residential proxies to avoid overloading the target site.

Apify and the actor author do not provide legal advice. You are solely responsible for ensuring your use of the extracted data complies with all applicable laws and regulations.

## Related

If you are building a B2B data pipeline, these actors complement Clutch.co Scraper:

- [LinkedIn Company Scraper](https://apify.com/automation-lab/linkedin-company-scraper) -- extract company profiles, employee counts, and industry data from LinkedIn
- [Google Maps Lead Finder](https://apify.com/automation-lab/google-maps-lead-finder) -- find local businesses with phone numbers, addresses, and reviews
- [Company Funding Tracker](https://apify.com/automation-lab/company-funding-tracker) -- track startup funding rounds and investor details
- [G2 Scraper](https://apify.com/automation-lab/g2-scraper) -- scrape software reviews and ratings from G2 for vendor comparison
- [Crunchbase Scraper](https://apify.com/automation-lab/crunchbase-scraper) -- collect company funding, leadership, and growth data from Crunchbase

Combine results from multiple scrapers to build enriched lead databases with ratings, funding history, and contact details in one dataset.