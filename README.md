# Data 512 A-1 Data curation and Analysis 


The overall goal of this project is to extact, transform and eventually analyze the pagecount data from wikipedia for the dates from Jan 2008 through Sep 2017, using api endpoints that are publicly available. 
The data is downloaded, and split into 5 raw JSON files each containing individual query results. More details about the files, and the links for the data can be found below

### License
The code is released under the MIT license, details for which can be found at the link below [https://github.com/Gmoog/data-512-a1/blob/master/LICENSE]

### Data

The data has been downloaded from the links provided below
https://wikimedia.org/api/rest_v1/#!/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end
https://wikimedia.org/api/rest_v1/#!/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end

The first link contains legacy data, from Jan 2008 to July 2016, of both mobile and desktop devices.
The second link contains data from mobile app, mobile web and desktop from July 2015 to Sep 2017. This project has filtered the data from this link to exclude spiders and crawlers, and pagecounts from other automated sources.

All usage is governed under wikipedias policy, which can be found at
https://foundation.wikimedia.org/wiki/Terms_of_Use/en

### Implementation

All details regarding data curation and analysis of the data, are explained in the jupyter notebook present in the same folder.

### Files
- pagecounts_desktop-site_200801-201607 -- legacy desktop data from 2008-2016
- pagecounts_mobile-site_200801-201607 -- legacy mobile data from 2008-2016
- pageviews_desktop-site_201507-201709 -- desktop data from 2015-2017
- pageviews_mobile-app-site_201507-201709 -- mobile app data from 2015-2017
- pageviews_mobile-web-site_201507-201709 -- mobile web data from 2015-2017
- en-wikipedia_traffic_200801-201709 -- final csv containing fields for analysis
- hcds-a1-data-curation -- jupyter notebook with all the implementation details

The list of fields in the csv file are detailed below
 - year	
 - month
 - pagecount_all_views -- total count of views (mobile + desktop) from the pagecount api
 - pagecount_desktop_views -- total desktop views from pagecount api
 - pagecount_mobile_views -- total mobile views from pagecount api
 - pageview_all_views -- total count of views (mobile + desktop) from pageview api
 - pageview_desktop_views -- total desktop views from pageview api
 - pageview_mobile_views -- total mobile views (web + app) from pageview api

### Things to Note
 - There is a 13 month period, during which the data overlaps, this can be seen in the visualization.
 - As briefly mentioned above, the pageview api has an option to filter data from bots and spiders, which is recommended in case the analysis is only concerned with user data.



