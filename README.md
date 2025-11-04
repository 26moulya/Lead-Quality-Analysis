Lead Quality Analysis – Analyst Case Study
 Overview

This project analyzes lead data from a single publisher and advertiser to identify lead quality trends, key performance drivers, and opportunities for improving conversion rates.

The dataset contains about 3,000 leads, each with attributes such as creation date, ad widget, campaign details, contact scores, and final call status.

 Objectives

Trend Analysis:
Determine whether lead quality is improving or declining over time and test for statistical significance.

Segmentation Analysis:
Identify which ad creatives, campaigns, partners, and customer segments generate the best-quality leads.

Optimization Strategy:
Evaluate if lead quality can be improved by 20% (from 8.0% → 9.6%) to justify a 20% increase in Cost Per Lead (CPL) from $30 → $33.
Dataset Description
Column	Description
Lead created date	Date the lead was generated.
CallStatus	Final disposition of the lead (Closed, EP Sent, Unable to Contact, etc.).
WidgetName	Internal name of the ad creative used.
PublisherZoneName	Page location where the ad appeared.
PublisherCampaignName	Campaign type (Online form vs. Call Center).
AddressScore	Validity of address (1–5 scale).
PhoneScore	Validity of phone number (1–5 scale).
AdvertiserCampaignName	Campaign brand (branded vs. generic).
State	State of the lead.
Debt level	Amount of debt reported by the consumer.
Partner	Advertising partner (Google, Yahoo, etc.).
Referral domain / Campaign / AdGroup / Keyword	Traffic and keyword metadata.
Analysis Steps

Data Cleaning

Standardized CallStatus into four quality groups:
Closed, Good (EP Sent/Received/Confirmed), Bad, Unknown.

Converted lead creation date to datetime and grouped by month.

Created binary indicators for closed and good-quality leads.

Trend Analysis

Monthly lead quality calculated as percentage of Closed or Good leads.

Linear regression and Spearman correlation used to test statistical significance of trend.

Segmentation Analysis

Calculated lead counts and conversion rates by:

WidgetName

PublisherCampaignName

AdvertiserCampaignName

Partner

State

AddressScore & PhoneScore

Debt Level Buckets

Visualization

Line chart for monthly closed rates.

Bar charts for top-performing widgets and partners.

Insights & Recommendations

Identified ad creatives and campaigns with highest closed rates.

Suggested focusing ad spend and optimization efforts on top-performing combinations.

Recommended address/phone score validation to filter poor-quality leads.

 Outputs
File	Description
analysis_report.txt	Summary of overall metrics, trends, and key insights.
monthly_closed_rate.png	Line chart showing monthly closed rate trend.
top_widgets_closed_rate.png	Bar chart of top 15 widgets by closed rate.
top_partners_closed_rate.png	Bar chart of top 15 partners by closed rate.
data_tables.xlsx (optional)	Consolidated tables for further visualization.
 Key Findings (to be filled after analysis)

Overall closed rate: ~8%

Lead quality trend: (increasing / decreasing)

Highest-performing widget: [WidgetName]

Top partner for conversions: [Partner]

AddressScore ≥ 4 and PhoneScore ≥ 4 lead to X% higher close rate

Leads with debt between 15k–30k show highest conversion

 How to Run

Open the analysis notebook or Python file (lead_quality_analysis.ipynb or .py).

Ensure required libraries are installed:

pip install pandas numpy matplotlib scipy openpyxl


Run the script to generate charts and the text report.

Author

Moulya K.B.
M.Tech in Computer Science & Engineering
Domain: Data Science & Artificial Intelligence
