![Header Image](assets/Slash_Proxies_header.png)

# Use Case: Provides access to core statistics on customer IP-proxy bandwidth usage rates and how they compare to other users.

# Authors
- [@slashdavid](https://github.com/slashdavid)

# Table of Contents
- [Business problem](https://github.com/slashdavid/slash-proxies-dashboard#business-problem)
- [Data Sources](https://github.com/slashdavid/slash-proxies-dashboard#data-sources)
- [Methods](https://github.com/slashdavid/slash-proxies-dashboard#methods)
- [Tech stack](https://github.com/slashdavid/slash-proxies-dashboard#tech-stack)
- [Quick view of dashboard](https://github.com/slashdavid/slash-proxies-dashboard#quick-view-of-dashboard)
- [Repository structure](https://github.com/slashdavid/slash-proxies-dashboard#repository-structure)

# Business problem
This dashboard allows me to obtain a clear perspective on company performance in relation to customer bandwidth usage patterns. When sourcing products from upstream providers, you're limited to the information that their platform aggregates, which is often quite limited. This dashboard solves this issue by organizing and displaying this information under a user-friendly design.

# Data sources
- Bandwidth statistics export from upstream residential proxy provider (subuser_bw_usage.csv)
- Export of monthly net sales volume from Slash Proxies Stripe account

# Methods
-

# Tech Stack
- Python
- Excel
- SQL
- Tableau

# Quick view of dashboard

# Repository structure
```

├── assets
│   ├── Slash_Proxies_header.png                  <- header image used in this readme file.
│
│
├── datasets
│   ├── subuser_bw_usage_sorted.csv
│   ├── active_users_by_date (2020-04 to 2021-01).csv
│   ├── total_bandwidth_usage_by_year_month (2020-04 to 2021-01).csv
│   ├── filtered_customers.json
│   ├── final_subuser_bw_usage.csv
│
│
├── README.md                                     <- this readme file.

```
