# web-table-template Setup

web-table-template loads and parses a CSV directly to create your interactive web table. 
Prep your CSV, reference it's location on the page stub, and you are ready to share.

You have three main options for your CSV:

- Google Sheets (you don't need to make it into a CSV!)
- a CSV available on the web
- a CSV directly in your project 

When your web table page loads, javascript downloads the CSV from the link you configured, parses it using the [Papa Parse](https://www.papaparse.com/) library, and then displays the results on the page.
Once the CSV is downloaded, the javascript stores it in the browser's session storage so that the data can be re-used with out downloading again as you navigate the site. 

If you want a fresh reload of the data (i.e. you made changes in Sheets and want to see the results), simply open the page in a new window!

## Set up Google Sheets

Set up a Google Sheet with metadata following the template.
Be especially careful with column names in the first row!
They need to have no spaces and no extra white space at the end of the value (and exactly match what you have used in configuring your collection site).

On the Sheet, go to File > Publish to the Web.
On the popup modal, use the dropdowns in "Link" tab to select the sheet name of your metadata (usually "Sheet 1") and "Comma-separated values (.csv)" options, then click "Publish" button.
Copy the link that is provided.

Paste link into "_config.yml" as value for `metadata-csv`.

For example: 

`metadata-csv: https://docs.google.com/spreadsheets/d/e/2PACX-1vSn7AA-cbsXT3_nNUGftc1ab-CKXOJHMQCIENeR9NHElbyI9_qA99o0-HNZdG04v-M2_N21bUe_krQQ/pub?gid=0&single=true&output=csv`

## Set up Web CSV

If you have a CSV available anywhere on the web, you can use it by referencing the full URL. 

For example:

`metadata-csv: https://www.lib.uidaho.edu/collectionbuilder/demo-metadata.csv`

Please ensure your CSV is correctly formatted and encoded (UTF-8), being especially careful with the column names.
We suggest creating your CSV using OpenRefine, Sheets, or LibreOffice Calc (and do not suggest using Excel, since Excel's CSV output is not correctly formatted).

## Use CSV in Project

Your CSV can also be hosted directly in your CB project.
Copy your CSV file into the "assets" folder then reference it in the "_config.yml" using a relative path. 

For example:

`metadata-csv: /assets/demo-metadata.csv`
