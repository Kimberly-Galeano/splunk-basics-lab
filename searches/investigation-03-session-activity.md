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
- Session-related authentication events were present in the dataset.
- Searches grouping session activity by user returned no results.
- Searches grouping session activity by source IP also returned no results.
- This indicates that user and source IP fields were not available or not extracted for session events in this dataset.
- No unusual or suspicious session activity could be identified based on the available data.
  
## Evidence
### Session Activity by User
This search returned no results, indicating that session events did not include an extracted user field.

![Session activity by user](./screenshots/investigation-03/session-activity-by-user.png)

### Session Activity by Source IP
This search returned no results, indicating that session events did not include an extracted source IP field.

![Session activity by source IP](./screenshots/investigation-03/session-activity-by-source-ip.png)

## Conclusion
This investigation reviewed session and successful login activity using Linux authentication logs in Splunk.

While session-related events were identified, the available logs did not include sufficient field data to analyze session activity by user or source IP. As a result, no abnormal session behavior could be confirmed.

This investigation demonstrates the ability to recognize data limitations, interpret incomplete log sources, and document findings accurately—an important skill in real-world security monitoring and analysis.
