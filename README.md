# Threat Hunting and Security Operations

Hands-on threat hunting labs and SOC investigations run through Microsoft Defender for Endpoint. Each scenario walks the full hunt lifecycle, from building a hypothesis to pulling logs with KQL, analyzing the data, investigating what turns up, and documenting the response.

The focus here is practical detection work, not theory. Every scenario uses real telemetry from live and honeypot VMs, hunts for actual attacker behavior like brute force attempts and lateral movement, and maps findings to the MITRE ATT&CK framework.

## Methodology

Every hunt follows the same seven-step structure so the work stays consistent and repeatable:

1. **Preparation.** Define the hypothesis based on threat intel and known security gaps.
2. **Data Collection.** Pull relevant logs from endpoints, network, and identity sources.
3. **Data Analysis.** Run KQL queries to surface anomalies, patterns, and IOCs.
4. **Investigation.** Dig into suspicious findings, scope the impact, and confirm the threat.
5. **Response.** Identify containment, eradication, and recovery actions.
6. **Documentation.** Record what was found and how.
7. **Improvement.** Note what would have prevented the activity or sharpened the hunt.

## Scenarios

| # | Scenario | Tactic | MITRE | Status |
|---|----------|--------|-------|--------|
| 01 | [Brute Force Login Detection](https://github.com/goubx/hunting-exposed-vm-bruteforce) | Credential Access | T1110 | Complete |
| 02 | [Sudden Network Slowdown](https://github.com/goubx/hunting-internal-port-scan/tree/main) | Discovery | T1046 | Complete |
| 03 | [Data Exfiltration](https://github.com/goubx/hunting-data-exfiltration/tree/main) | Collection | T1005 | Complete |
## Repo Structure

```
threat-hunting-soc/
  README.md
  scenario-01-brute-force/
    README.md
    queries.kql
    screenshots/
  scenario-template/
    README.md
```

Each scenario folder is self-contained. It holds the hunt setup, the KQL queries used, screenshots of the findings, a timeline of events, and a writeup covering response and prevention.

## Tools

- Microsoft Defender for Endpoint (Advanced Hunting)
- Kusto Query Language (KQL)
- MITRE ATT&CK Framework

## About

Built and maintained by Mohamed Yagoub as part of ongoing detection and response work. More scenarios get added as they are completed.
