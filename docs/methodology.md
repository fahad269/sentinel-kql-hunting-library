# Methodology

## How queries were developed

- Built from publicly documented attack techniques (MITRE ATT&CK,
  vendor threat intelligence blogs, public incident reports)
- Validated for KQL syntax correctness against Microsoft Sentinel /
  Log Analytics demo data or a personal lab workspace
- False-positive guidance derived from general operational experience
  in SOC environments, written generically (no employer-specific data)

## What this library is not

- Not a copy of any employer's, client's, or vendor's proprietary
  detection content
- Not production-ready without tuning to your specific environment,
  log volume, and baseline behavior

## Versioning

- Queries are dated at last update
- Breaking changes to query logic will be noted in commit messages
