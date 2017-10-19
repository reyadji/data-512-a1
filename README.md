# data-512-a1

## A1: Data Curation

### Requirement
To mine, construct, visualize, and publish datset of monthly traffic on English Wikipedia from January 2008 through SEptember 2017.


### Pre-requisite
Here's the pre-requisite to build the report:
- Python3
- Jupyter Notebook
- Built-in Python 3 library, such as json, csv, pprint
- Additional Python 3 packages: pandas, requests, ggplot (optional)


### Wikipedia API
For this project, I am using two different Wikimedia API endpoints,
1. Pagecounts API endpoint(https://wikimedia.org/api/rest_v1/#!/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end) is documented here(https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts).
2. Pageviews API endpoint(https://wikimedia.org/api/rest_v1/#!/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end) is documented here (https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews).



### Outputs
If all cells of the Jupyter notebook was ran, it would produce 5 JSON files (pagecounts' mobile and desktop, and pageviews' mobile-app, mobile-web, and desktop), which in turn is combined to provide a single comprehensive CSV file with the following headers:
- year
- month
- pagecounts_desktop_views: number of visits from desktop user
- pagecounts_mobile_views: number of visits from mobile user
- pagecounts_all_views: pagecount desktop views + pagecount mobile views
- pageviews_desktop_views: number of visits from desktop user
- pageviews_mobile_views: number of visits from mobile app user + number of visits from desktop user from mobile web user
- pageviews_all_views: pageview desktop views + pageview mobile views

The final output is a png file of those number of views in one plot.


### Issues
A couple issues I have encountered are missing necessary packages on the Python virtual environment (see above for list of Python packages) and trying to manipulate the data with basic Python data structure (data munging becomes much easier when I started using pandas dataframe). 


### License
MIT License

Copyright (c) October 18, 2017 Reynaldo Adji adjir@uw.edu

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
