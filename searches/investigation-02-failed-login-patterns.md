# Splunk Investigation 02 – Failed Login Pattern Analysis

## Objective
Analyze failed authentication events to identify repeated login failures, user patterns, or potential indicators of brute-force activity.

## Environment
- Splunk (Free / Training Environment)

## Data Source
- Linux authentication logs (auth.log)

## SPL Queries Used

## Failed password events
```spl

index=main "Failed password"
| stats count by user
| sort - count
```
## Failed logins by source IP
```spl
index=main "Failed password"
| stats count by src_ip
| sort - count
```
## Findings
Pending analysis. Searches will be executed in Splunk to identify failed login patterns.

## Evidence
Screenshots will be added after searches are completed.

## Conclusion
Pending investigation results.
