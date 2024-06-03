# Web Scraping Project

## Overview

This project involves scraping marketing-relevant information from both list and product pages on three different e-commerce websites. The goal is to extract data such as product names, prices, discounted prices, brands, and product descriptions, and save this information into a structured CSV file for further analysis.

## Task Description

### Task 2: Webscraping

- **Objective:** Scrape marketing relevant information from list and product pages on three different websites.
- **List Pages:** Contain more than one product.
- **Product Pages:** Dedicated to a single product.

### Data to be Collected

#### From List Pages:
- Product name
- Price
- Discounted price (if available)
- Position

#### From Product Pages:
- Brand
- Number of photos
- Colors
- Product description

### Output
- Arrange output in a CSV file with the following columns:
  - URL
  - List/Product page
  - Product name
  - Brand
  - Price
  - Discounted price
  - Position
  - Number of photos
  - Number of colors
  - Product description

## Websites and URLs

### List Page URLs
1. [Miss Etam - Dresses](https://www.missetam.nl/nl/collectie/jurken/)
2. [Gap - Women's Jeans](https://www.gap.com/browse/category.do?cid=5664&nav=meganav%3AWomen%3ACategories%3AJeans#pageId=0&department=136)
3. [Your Look for Less - Blouses](https://www.your-look-for-less.nl/goedkope-blouses)

### Product Page URLs
1. [Miss Etam - Top Print Zwart](https://www.missetam.nl/nl/3844173/top-print-zwart/)
2. [Gap - Product Example](https://www.gap.com/browse/product.do?pid=794603002&rrec=true&mlink=5001,1,dynamicerror_gapoos1_rr_2&clink=1#pdp-page-content)
3. [Your Look for Less - Product Example](https://www.your-look-for-less.nl/p/99055)

## Implementation Details

### Libraries Used
- `requests`
- `BeautifulSoup`
- `selenium`
- `pandas`
- `googletrans`

### Steps for Scraping

1. **Setup WebDriver:**
   - Use Selenium WebDriver to automate browser interactions.
   - Configure Chrome to run in headless mode.

2. **Scrape List Pages:**
   - Navigate to each list page URL.
   - Extract product names, prices, discounted prices, and positions of the first 10 products.
   - Collect product URLs for further details.

3. **Scrape Product Pages:**
   - Navigate to each product URL obtained from list pages.
   - Extract additional details such as brand, number of photos, colors, and product description.
   - Translate product descriptions to English if necessary.

4. **Data Storage:**
   - Store all scraped data in a Pandas DataFrame.
   - Save the DataFrame to a CSV file.

## Running the Code

1. Ensure you have the required libraries installed. You can install them using pip:
   ```sh
   pip install requests beautifulsoup4 selenium pandas googletrans
