# Fuse Service — Marketing Dashboard
Standalone HTML marketing dashboard for Fuse Service: Heating & Air Conditioning. No server, no build step — a single self-contained file that runs directly in the browser.
Live: ihor-ihnatiev.github.io/fuse-dashboard

What it does
Tracks marketing performance across all lead channels in one place — ad spend, funnel metrics, revenue, and ROI — with CSV import from Google Ads, Facebook Ads, Yelp, and Housecall Pro.
Channels covered
ChannelTabNotesGoogle Ads✅ Dedicated tabCampaigns + keywordsFacebook Ads✅ Dedicated tabAd setsYelp✅ Dedicated tabCampaigns + keywordsThumbtack✅ Dedicated tabLSA✅ Dedicated tabLocal Services AdsReserve with Google✅ Dedicated tabOnline Booking✅ Dedicated tabRegular✅ Dedicated tabReturning clientsRecommendation✅ Dedicated tabWord of mouth

Features
📊 Overview
Summary table of all sources with KPI cards (Revenue, Ad Spend, Gross Profit, Gross ROI, ROAS, Cost per Booking) and three charts: Revenue by source, Lead→Booking rate, Gross ROI %.
Per-source tabs
Each paid channel gets a dedicated page with:

8 KPI cards — Spend, Revenue, Gross Profit, ROI, Impressions, Clicks, Leads, Booked
Campaign table — switchable between Funnel view (Impressions → Clicks → Leads → Booked) and Finance view (Spend → Revenue → COGS → Gross Profit → ROAS → ROI)
Keywords table — with CSV import, inline editing, checkbox multi-select delete
Monthly comparison cards — when 2+ months are selected
Charts — Revenue vs Spend by campaign, Revenue trend by month

📋 Housecall tab
Upload a Housecall Pro Jobs CSV export to get end-to-end attribution:

Full funnel: Leads → Scheduled → Jobs → Completed → Revenue
Revenue breakdown by lead source with ROAS and ROI (matched against ad spend from the dashboard)
Job type breakdown: Service / Installation / Estimate / Maintenance
Monthly revenue and jobs charts
On import, automatically updates Revenue in the corresponding source tabs


CSV import formats supported
SourceFormatKey columnsGoogle Ads (campaigns)Time-series reportDate, Impressions, Clicks, Conversions, CostGoogle Ads (keywords)Keyword reportSearch keyword, Match type, Impressions, Clicks, CostFacebook AdsAd set reportAd set name, Amount spent, Impressions, ResultsYelp (campaigns)Business reportTime Period, Billed Ad Impressions, Billed Ad Clicks, Ad Costs, Rax and MTBYelp (keywords)Search terms reportSearch Term, Delivered Ad Impressions, Billed Ad Clicks, Ad CostsHousecall ProJobs exportJob lead source, Job revenue, Job type, Job status
Delimiter auto-detected (comma or tab). Duplicate keywords are merged, not duplicated.

How to use
Adding a month
Click 📅 Добавить → pick a month from the calendar. The new month is pre-populated with the same source/campaign structure as the latest existing month (with zeroed metrics).
Entering data
Select a month tab → navigate to a source → edit cells directly in the table. All edits auto-save to localStorage.
Importing CSV
Hover over a campaign row → click ⬆ → select the CSV file. For keywords, use the ⬆ Импорт CSV button in the Keywords section header.
Housecall Pro sync
Go to 📋 Housecall tab → drag and drop (or click to upload) the Jobs export CSV from Housecall Pro. Revenue is automatically pushed to matching source tabs.
Multi-month view
Select multiple month tabs → click All ∑ to aggregate all selected months. All metrics are summed; read-only mode activates (no editing in aggregate view).

Data storage
All data is stored in browser localStorage (fuse_v7 key). Data is local to the browser — it does not sync across devices. To back up or transfer data, use browser dev tools → Application → Local Storage → copy the fuse_v7 value.

Tech stack

Vanilla HTML + CSS + JavaScript — zero dependencies, zero build step
Chart.js 4.4.1 via CDN — charts only
localStorage — persistence


Files
fuse-dashboard.html   — the entire dashboard (single file)
README.md             — this file

Development
All logic lives in fuse-dashboard.html. To make changes:

Edit the file locally or in GitHub Codespaces
Commit and push — GitHub Pages deploys automatically

bashgit add fuse-dashboard.html
git commit -m "describe change"
git push

Fuse Service: Heating & Air Conditioning · fusesea.com · (425) 380-4300
