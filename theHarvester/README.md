# theHarvester - OSINT Tool Learning

## Overview
This repository documents my hands-on learning experience with **theHarvester** OSINT tool as part of the **Security Blue Team - BJPT Bundle (Intro to OSINT path)**.

The goal of this exercise was not just to run the tool, but to understand:
- How passive OSINT works
- Common tool and environment issues
- Backend limitations and noisy results
- How analysts interpret and document findings responsibly

---

## Learning Objectives
- Understand passive reconnaissance concepts
- Use theHarvester to collect publicly available information
- Identify and fix common CLI and environment issues
- Recognize false positives and data noise
- Document observations clearly from a blue-team perspective

---

## Tool Usage

### Basic Command Structure
```bash
theHarvester -d <domain> -b <backend(source)> -l <limit>
```

### Example Commands Used
```bash
theHarvester -d example.com -b all
theHarvester -d example.com -b google -l 500
theHarvester -d example.com -b bing
theHarvester -d example.com -b duckduckgo
theHarvester -d example.com -b crtsh
theHarvester -d brave.com -b crtsh
```

## Backend Observations
- Google backend frequently returns no results due to rate limiting and bot detection
- Certificate Transparency (crt.sh) provides reliable subdomain data
- Using -b all returns a large volume of results, including unrelated or historical domains
- OSINT tools rely heavily on third-party data sources, which may be outdated or incomplete

## Passive Recon Findings
Additional passive reconnaissance was conducted using public platforms, such as URLScan. 

## The collected URLs, IPs, and hosts represent:
- Historical observations of website activity
- External resources and third-party services
- CDN and infrastructure exposure

No active scanning or direct interaction was performed

## Blue Team Relevance
- Helps identify an organization's external attack surface
- Supports asset visibility and exposure awareness
- Demonstrates why validation is critical in SOC workflows
- Highlights how OSINT data should be treated as informational, not authoritative

## Key Takeaways 
- Tool misconfiguration leads to misleading results
- OSINT data contains noise and false positives
- Backend choice directly affects output quality
- Documentation and analyst judgment are essential skills

  


  
