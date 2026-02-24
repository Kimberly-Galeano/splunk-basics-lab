# Splunk Investigation 04 – Windows Authentication & Privilege Review

## Objective
Analyze Windows authentication and privilege-related events to identify successful logins, failed login attempts, and potential privileged activity.

## Environment
- Windows OS
- Splunk (Free / Training Environment)

## Data Source
- Windows Security Event Logs

## SPL Queries Used

### Successful logons
```spl
EventCode=4624
```
### Failed logons
```spl
EventCode=4625
```
### Privileged logons
```spl
EventCode=4672
```
## Findings
Pending analysis. Searches will be executed after ingesting Windows Security logs into Splunk.

## Evidence
Screenshots will be added after searches are completed.

## Conclusion
Pending investigation results.
