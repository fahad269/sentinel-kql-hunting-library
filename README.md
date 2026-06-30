# Sentinel KQL Hunting Library

A curated library of Microsoft Sentinel hunting and detection queries,
mapped to MITRE ATT\&CK, spanning identity, endpoint, network, cloud,
data exfiltration, and insider threat domains.

Built from practical detection engineering concepts, this library is intended
as both a learning resource and a starting point for security teams building
out their Sentinel hunting program.

## Why This Exists

Most public KQL repositories focus narrowly on one domain (usually endpoint
or identity) and rarely document false-positive tuning or MITRE mapping in a
consistent way. This library aims to:

* Cover the full attack surface a typical SOC needs to hunt across
* Make every query immediately usable, not just illustrative
* Document the "why," not just the "what," behind each detection

## Structure

|Folder|Domain|Query Count|
|-|-|-|
|`/identity`|Identity \& Access (Entra ID)|6|
|`/endpoint`|Endpoint (Defender for Endpoint)|6|
|`/network`|Network / Firewall|5|
|`/cloud`|Azure Cloud Security|5|
|`/data-exfiltration`|Data Loss / Exfiltration|4|
|`/insider-threat`|Insider Threat \& Anomalous Behavior|4|

> Build status: Identity domain complete. Remaining domains in progress.

## MITRE ATT\&CK Coverage

See [docs/mitre-coverage-matrix.md](docs/mitre-coverage-matrix.md) for the
full technique-to-query mapping.

## How to Use

Each query file includes:

* MITRE ATT\&CK technique mapping
* Required Sentinel/Log Analytics data source
* Detection rationale
* False-positive tuning guidance

Copy the query body into Sentinel's Logs blade or a custom Analytics Rule.
All queries require validation and threshold tuning against your own
environment before production deployment.

## Methodology

See [docs/methodology.md](docs/methodology.md) for how queries in this
repo were designed and validated.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## Disclaimer

These queries are illustrative, built from general threat-hunting concepts,
public threat intelligence, and MITRE ATT\&CK documentation. They contain no
proprietary logic, thresholds, or data from any employer or client
environment. Validate and tune thoroughly before production use.

## Author

Muhammad Fahad — Information Security Analyst specializing in security
operations, GRC, and detection engineering.

https://www.linkedin.com/in/muhammadfahad-infosec | https://github.com/fahad269

## License

Released under the MIT License. See [LICENSE](LICENSE).

