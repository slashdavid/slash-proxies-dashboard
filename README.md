![Header Image](assets/Slash_Proxies_header.png)

# Use Case: Provides ease of access to core statistics on global and specific customer IP-proxy bandwidth usage rates.

# Business problem
This dashboard allows me to obtain a clear perspective on company performance in relation to customer bandwidth usage patterns. When sourcing residenital proxies from upstream providers, you're limited to the information that their platform aggregates, which is often quite limited. This dashboard solves this issue by organizing and displaying this information under a user-friendly design.

# Data Collection
As this project was inspired by my IP-proxy company, Slash Proxies, I was able to receive exports of user bandwidth usage statisics from our upstream provider and financial summaries from our company Stripe account.

However, I had to restore old company database files through MongoDB Shell.

Exact procedure can be found in the [MongoDB File Recovery](documentation/mongodb_file_recovery.md) documentation file.

# Data Cleansing
Multiple cleansing procedures such as:
- Removing portions of bugged strings
- Removing unneeded fields from JSON files
- JSON to CSV parsing

Procedures can be found within the [Data Formatting](documentation/data_formatting.ipynb) notebook.

# Tech Stack
- Python
- SQL
- Tableau

# Quick view of dashboard
[Link to Tableau Public](https://public.tableau.com/app/profile/david.zhang2464/viz/CustomerBandwidthUsageDashboard/Dashboard?publish=yes)

![Dashboard Gif](assets/dashboard.gif)

# Repository structure
```


├── analysis_files
│   ├── final_files
│      ├── active_users_by_date.csv               <- the dataset with # of active users grouped by date.
│      ├── filtered_customers.json                <- the dataset with all required customer info (contains placeholder data).
│      ├── final_subuser_bw_usage.csv             <- the dataset with data matched subuser and customer information.
│      ├── subuser_bw_usage_sorted.csv            <- the dataset with all subusers and their bandwidth usage by date.
│      ├── total_bandwidth_usage_by_date.csv      <- the dataset with total bandwidth grouped by date.
│   ├── unclean
│      ├── subuser_bw_usage.csv                   <- the dataset with unorganized subuser information.
│
│
├── assets
│   ├── Slash_Proxies_header.png                  <- the header image used in the readme file.
│   ├── dashboard.gif                             <- the gif used in the readme file.
│
│
├── documentation
│   ├── data_formatting.ipynb                     <- the jupyter notebook that documents my data cleansing process.
│   ├── mongodb_file_recovery.md                  <- the md file that documents my process of recovering customer data with mongodb.
│
│
├── README.md                                     <- this readme file.


```
