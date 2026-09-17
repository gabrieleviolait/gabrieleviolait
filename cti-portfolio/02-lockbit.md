# Case Study 02 — LockBit 3.0 / 4.0 / 5.0
## Ransomware-as-a-Service resilience after Operation Cronos

**Focus:** Ransomware · Tor monitoring · Data Leak Sites · RaaS ecosystem · Law-enforcement disruption  
**Research type:** Independent, passive CTI research  
**Analyst background:** Historical passive monitoring of LockBit-associated leak infrastructure and actor-controlled sources, correlated with law-enforcement and technical reporting.

> **Publication note:** This public version intentionally omits live onion addresses, access-enabling details, victim-specific raw material and operationally sensitive source information.

## Intelligence Requirement

**To what extent did Operation Cronos disrupt LockBit as an organisation, and what did subsequent attempts to relaunch infrastructure and develop later LockBit generations reveal about the resilience of the underlying RaaS ecosystem?**

## Analytic model

A ransomware brand should not be assessed only by whether new malware or a new leak site exists.

A functioning RaaS ecosystem depends on multiple components:

`Malware + Infrastructure + Affiliates + Reputation + Negotiation capability + Payment channels + OPSEC`

A disruption campaign that damages several of these elements simultaneously may have effects that are not visible from malware samples alone.

## Key findings

### 1. Operation Cronos compromised the operational core of LockBit

In February 2024, the international Operation Cronos compromised LockBit's primary platform and critical infrastructure. Europol reported the takedown of 34 servers across multiple countries, arrests, indictments and the freezing of more than 200 cryptocurrency accounts linked to the criminal organisation.

The UK's National Crime Agency took control of LockBit's primary administration environment and public-facing dark-web leak site. The investigation also obtained source code and intelligence concerning the affiliate network.

### 2. The affiliate network was directly exposed

NCA reporting identified **194 affiliates** associated with LockBit before the February 2024 disruption. The NCA later reported that the number of active affiliates had significantly decreased following the operation.

This matters because a RaaS brand is partly a trust market. Affiliates choose an operator based on reliability, access to infrastructure, expected revenue, support and perceived OPSEC. Law-enforcement access to backend systems can therefore damage a RaaS even if the malware itself remains technically functional.

### 3. Relaunch activity did not equal full recovery

LockBit rapidly attempted to re-establish public-facing infrastructure. However, NCA and Trend Micro reporting described reduced activity, reputational damage and the reuse or inflation of victim claims after the takedown.

The relevant CTI question is therefore not:

> "Did LockBit come back online?"

but:

> "Did LockBit restore its previous operational capacity, affiliate confidence and ecosystem health?"

These are different questions.

### 4. LockBit-NG-Dev / version 4.0 showed technical adaptation under ecosystem pressure

Trend Micro, working with the NCA, analysed an in-development LockBit codebase tracked as **LockBit-NG-Dev**, associated with the group's attempt to evolve toward a new generation / version 4.0.

The existence of a new codebase demonstrates continued technical development, but it does not by itself prove that the surrounding RaaS ecosystem recovered. Malware capability and organisational resilience need to be assessed separately.

### 5. Later LockBit 5.0-branded infrastructure is a continuity signal, not proof of full recovery

**Current analyst observation — 17 September 2026:** I directly observed a **LockBit 5.0-branded leak portal** accessible through Tor. The public portfolio intentionally omits the live onion address and raw victim-list material.

This observation supports a narrow conclusion with **high confidence**: LockBit-branded public-facing infrastructure remained operationally present at the time of observation.

It does **not** automatically prove that:

- every listed victim claim is accurate;
- every incident was conducted by the same core operators;
- affiliate participation returned to pre-Cronos levels;
- ecosystem trust, negotiation capacity or revenue fully recovered.

For CTI purposes, the existence of a current leak site should therefore be treated as **infrastructure / brand continuity evidence**, then correlated with independent incident reporting, affiliate activity, malware telemetry and law-enforcement intelligence.

## Analytic assessment

**High confidence:** Operation Cronos materially degraded LockBit's infrastructure and exposed its affiliate ecosystem.

**High confidence:** LockBit attempted to rebuild public-facing infrastructure and continue development after the disruption.

**High confidence:** LockBit 5.0-branded public-facing infrastructure was directly observable by the analyst on 17 September 2026.

**Moderate confidence:** The long-term health of the RaaS brand after disruption depends substantially on affiliate trust, recruitment, infrastructure security and reputation, not only on availability of a new ransomware build or leak portal.

The case demonstrates why CTI should distinguish:

- **malware intelligence** — what the code can do;
- **infrastructure intelligence** — where services operate and how they are organised;
- **actor intelligence** — who operates or supports the ecosystem;
- **ecosystem intelligence** — whether affiliates, reputation and criminal services remain viable.

## MITRE ATT&CK

A core technique commonly associated with LockBit affiliate operations is:

- **T1486 — Data Encrypted for Impact**

Other techniques should be mapped to specific affiliate intrusions or independently documented campaigns. A RaaS operator's brand should not be used to automatically attribute every affiliate's full intrusion chain.

## Intelligence gaps

- How many affiliates remained operationally loyal after major disruption phases?
- Which post-disruption victim claims reflected genuinely new LockBit activity versus recycled or misattributed activity?
- How did reputation damage affect recruitment and negotiations compared with purely technical disruption?
- To what extent did later versions restore capability without restoring ecosystem trust?
- Which current LockBit 5.0 claims can be independently corroborated by victim disclosures, incident-response reporting or external telemetry?

## Skills demonstrated

- ransomware leak-site monitoring;
- RaaS ecosystem analysis;
- current-source observation and provenance handling;
- separation of malware and organisational intelligence;
- law-enforcement disruption assessment;
- source validation and confidence language;
- longitudinal threat-actor tracking.

## Public sources

1. Europol — *Law enforcement disrupt world's biggest ransomware operation*: https://www.europol.europa.eu/media-press/newsroom/news/law-enforcement-disrupt-worlds-biggest-ransomware-operation
2. UK National Crime Agency — *The NCA announces the disruption of LockBit with Operation Cronos*: https://www.nationalcrimeagency.gov.uk/the-nca-announces-the-disruption-of-lockbit-with-operation-cronos
3. UK National Crime Agency — *LockBit leader unmasked and sanctioned*: https://nationalcrimeagency.gov.uk/news/lockbit-leader-unmasked-and-sanctioned
4. Trend Micro — *LockBit's Struggle for Survival: Analyzing the Decline and Potential Resurgence with Version 4.0*: https://www.trendmicro.com/content/dam/trendmicro/global/en/core/docs/misc/lockbit-summary.pdf
5. Trend Micro — LockBit / Operation Cronos research overview: https://www.trendmicro.com/it_it/lockbit-ng-dev-prevent.html

---

**Analyst:** Gabriele Viola  
**Portfolio:** [Back to CTI Portfolio](README.md)
