# Learning Notes -theHarvester

## Environment Setup Issues
- Initially unable to install theHarvester using
  ```bash
  sudo apt install theHarvester
  ```
- Error messages indicated missing or misconfigured Kali Linux package sources.
- Fixed by updating '/etc/apt/sources.list' with Kali rolling repo:
  ```bash
  deb http://http.kali.org/kali kali-rolling main contrib non-free non-free-firmware
  ```
  After running sudo apt update, the installation worked fine.

## Command Usage Mistakes

Ran this incorrect command initially:
```bash
theHarvester -b example.com -l 500 -d google
```
Issue: used -d instead of -b to specify backend 

Correct command:
```bash
theHarvester -d example.com -b google -l 500
```
Also learned to use -b all to get data from all sources, but the results were overwhelming.

## Data Noise and Backend Confusion

- Using -b all returned a huge number of domains, many unrelated or historical.
- Certificate Transparency backend (crt.sh) gave more reliable subdomain data.
- Google backend mostly returned no results, likely due to rate limiting or bot detection.
- Learned that OSINT tools rely on third-party data, which can be outdated or noisy.
- Realized the importance of manually validating and deduping results.

## General Observations
- Screenshots were taken only for command usage; no screenshots of errors or fixes.
- Screenshots are helpful, but written explanations are sufficient.
- Important takeaway: knowing what the tool does, its limitations, and documenting findings clearly is key.
- SOC analysts often work with incomplete or noisy data and must validate everything.
