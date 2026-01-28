# Splunk Basics Lab

## Overview
This repo documents my beginner Splunk practice using searches to find useful events in logs and understand what “normal” activity looks like.

## Tools Used
- Splunk (free/training environment)
- Sample data / lab data

## What I Practiced
- Running basic searches and filtering results
- Finding login-related events and errors
- Narrowing results using keywords and time ranges
- Saving searches and documenting what I found

## Example Searches (starter)
These are beginner examples I practiced (I’ll expand these as I go):
- `index=* error OR failed OR failure`
- `index=* (login OR logon OR authentication)`
- `index=* sourcetype=* | head 20`

## Notes
More screenshots and findings will be added as I continue improving my searches and documentation.
