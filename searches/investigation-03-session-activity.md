# Splunk Investigation 03 – Session Activity & Successful Login Review

## Objective
Review successful login and session activity to identify normal user behavior and detect any unusual or unexpected session patterns.

## Environment
- Splunk (Free / Training Environment)

## Data Source
- Linux authentication logs (auth.log)

## SPL Queries Used

### Successful login events
```spl
index=main ("Accepted password" OR "session opened")
```
### Session activity by user
```spl
index=main "session opened"
| stats count by user
| sort - count
```
### Session activity by source IP
```spl
index=main "session opened"
| stats count by src_ip
| sort - count
```
## Findings
Pending analysis. Searches will be executed in Splunk to evaluate session activity patterns.

## Evidence
Screenshots will be added after searches are completed.

## Conclusion
Pending investigation results.
