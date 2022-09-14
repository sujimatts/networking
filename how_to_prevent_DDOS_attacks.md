### 1. AWS Shield
AWS Shield is a managed Distributed Denial of Service (DDoS) protection service that safeguards applications running on AWS. AWS Shield provides always-on detection and automatic inline mitigations that minimize application downtime and latency, so there is no need to engage AWS Support to benefit from DDoS protection. There are two tiers of AWS Shield - Standard and Advanced.

All AWS customers benefit from the automatic protections of AWS Shield Standard, at no additional charge. AWS Shield Standard defends against most common, frequently occurring network and transport layer DDoS attacks that target your web site or applications. When you use AWS Shield Standard with Amazon CloudFront and Amazon Route 53, you receive comprehensive availability protection against all known infrastructure (Layer 3 and 4) attacks.

https://aws.amazon.com/shield/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc

### How it works
```https://docs.aws.amazon.com/waf/latest/developerguide/ddos-overview.html```

### 2. Cloudflare

Cloudflare DDoS protection secures websites, applications, and entire networks while ensuring the performance of legitimate traffic is not compromised.

https://support.cloudflare.com/hc/en-us/articles/200172676-Understanding-Cloudflare-DDoS-protection

### Basic Actions
- Detect sudden increase in HTTP error rates(above threshold eg: 1,000 errors-per-second rate threshold)
- HTTP errors in the 52X range (Internal Server Error) and in the 53X range, except for error 530.
- IP Access Rules - Recommended for blocking multiple IP addresses, /16 or /24 IP ranges, or Autonomous System Numbers (ASNs). 
- User Agent Blocking - Recommended for blocking suspicious User-Agent headers for your entire domain.
- Firewall rules - Recommended for blocking a country, any valid IP range, or more complex attack patterns.
