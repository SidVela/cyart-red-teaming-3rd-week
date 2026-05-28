# Shodan Apache Reconnaissance

## Objective
Identify publicly exposed Apache servers using Shodan.

## Query Used

```text
apache country:US
```

## Findings

| IP Address | Organization | Service | Notes |
|------------|-------------|---------|------|
| 74.63.238.114 | Limestone Networks | Apache HTTP Server | HTTP redirect response identified |
| 52.53.125.73 | Amazon Technologies Inc. | Apache/2.4.54 | Apache running on Unix with OpenSSL |
| 54.205.237.21 | Amazon.com Inc. | Apache Service Center | Management appliance exposed |

## Observations

- Apache services were publicly accessible.
- HTTP response headers exposed server technologies.
- Some systems revealed Apache versions and OpenSSL details.
- Public infrastructure metadata can assist attackers during reconnaissance.

## MITRE ATT&CK Mapping

| Technique | ID |
|-----------|----|
| Active Scanning | T1595 |
| Gather Victim Network Information | T1590 |

## Security Risks

- Version disclosure
- Public-facing service exposure
- Potential outdated Apache versions
- Information leakage through banners

## Recommendations

- Disable unnecessary banner disclosure
- Update Apache and OpenSSL
- Restrict public exposure
- Implement WAF protection
- Monitor suspicious scanning activity

## Conclusion

Shodan successfully identified exposed Apache web servers and infrastructure metadata through passive reconnaissance techniques. The collected information demonstrates how attackers can enumerate internet-facing systems before exploitation attempts.
