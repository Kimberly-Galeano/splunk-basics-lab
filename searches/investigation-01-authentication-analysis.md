# Splunk Investigation 01 – Authentication Analysis

## Objective
Identify failed logins, successful logins, and unusual authentication patterns using Splunk searches.

## Environment
- Splunk (Free / Training Environment)

## Data Source
- Sample authentication and security events

## SPL Queries Used
```spl
index=* authentication
index=* (failed OR failure)
index=* (success OR accepted)
index=* (failed OR failure)
| stats count by user, src_ip
| sort - count
```
## Findings
- Pending. Results will be documented after running searches in Splunk.

## Conclusion
- Pending analysis.

## Evidence
- Screenshots will be added after running the SPL searches.
