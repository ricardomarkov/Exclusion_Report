# Google Ads U.S. Clicks Report Script

## Overview
This Google Ads Script generates a **report of campaigns that received clicks from the U.S.** over the last 90 days and sends an email to specified recipients.

## Features
✅ Scans the **last 90 days** of data across all campaigns.  
✅ Identifies campaigns that **received clicks from the U.S. (Country ID: 2840)**.  
✅ Sends an **email report**.
✅ Logs the results in **Google Ads Scripts Console**.  

## How It Works
1. The script queries the **GEO_PERFORMANCE_REPORT** for campaigns that had U.S. clicks in the last 90 days.
2. It checks if any campaign received **clicks from the U.S. (Country ID: 2840)**.
3. If there are U.S. clicks, it collects **Campaign Name, Clicks, and Impressions**.
4. The script **emails the report** to the designated recipients.
5. If no U.S. clicks are detected, it logs: _"No U.S. clicks detected in the last 90 days."_

## Setup Instructions
1. **Go to Google Ads** → Tools & Settings → Scripts.
2. **Create a new script** and paste the provided code.
3. **Authorize the script** when prompted.
4. **Schedule it to run weekly or monthly** (Recommended: Weekly for ongoing monitoring).
5. **Monitor email reports** to track any U.S. clicks.

## Customization
🔹 Want to modify email recipients? Update the `EMAILS` array in the script.  
🔹 Need a different time frame? Change `DURING LAST_90_DAYS` in the query.  
🔹 Want to track other countries? Modify `CountryCriteriaId = 2840` to the desired country ID.  

## Example Email Output
```
Subject: Google Ads Report: U.S. Clicks Detected

The following campaigns received clicks from the U.S. in the last 90 days:

Campaign A - Clicks: 50, Impressions: 1,000
Campaign B - Clicks: 20, Impressions: 500
```

## Notes
- This script **does not exclude U.S. traffic**; it only reports on it.
- Ensure that your **Google Ads account has email permissions** to send reports.
- Review logs in the Google Ads Scripts interface for execution details.


