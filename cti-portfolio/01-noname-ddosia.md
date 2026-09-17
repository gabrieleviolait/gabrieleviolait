# Case Study 01 — NoName057(16) / DDoSia
## Monitoring a volunteer-driven hacktivist DDoS ecosystem

**Focus:** Hacktivism · Telegram monitoring · DDoS infrastructure · OSINT/CLOSINT · Threat-actor tracking  
**Research type:** Independent, passive CTI research  
**Analyst background:** Historical passive observation of actor-associated Telegram/community sources, correlated with public technical and law-enforcement reporting.

> **Publication note:** This public case study is sanitized. It does not publish live access points, private invitations, research identities or operationally useful infrastructure details.

## Intelligence Requirement

**How does NoName057(16) translate ideological messaging and community mobilisation into coordinated DDoS activity, and which observable signals are useful for understanding targeting and operational structure?**

## Collection approach

The case separates four evidence types:

1. **Actor-controlled communications** — useful for messaging, claimed targets and mobilisation.
2. **Technical infrastructure research** — useful for understanding DDoSia delivery, C2 architecture and target distribution.
3. **Independent impact reporting** — useful for checking whether claims correspond to observable disruption.
4. **Law-enforcement reporting** — useful for validating structure, scale and disruption outcomes.

An actor claim is therefore recorded as a **claim** until independently corroborated.

## Key findings

### 1. Telegram is part of the operational ecosystem, not only a propaganda channel

NoName057(16) has used public and community-facing channels to communicate political narratives, announce targets and mobilise supporters. Early SentinelLabs research documented the group's Telegram presence, a volunteer-fuelled DDoS participation model and DDoSia tooling across multiple operating systems.

This makes messaging channels useful CTI sources for:

- target-selection patterns;
- timing of campaigns;
- mobilisation and recruitment;
- narrative framing;
- changes in operational tempo.

### 2. DDoSia adds central coordination to a distributed supporter model

Public technical research shows that DDoSia distributed target instructions to participating systems rather than relying on fully independent volunteer target selection. Later Recorded Future analysis described a multi-tier C2 architecture and tracked more than 3,700 unique targeted hosts between July 2024 and July 2025, with spikes linked to geopolitical developments.

This suggests an important distinction:

`Distributed participants ≠ fully decentralised operation`

The public-facing ecosystem can appear loose and volunteer-driven while target tasking and supporting infrastructure remain centrally organised.

### 3. Claimed success must be separated from confirmed impact

Hacktivist groups benefit reputationally from publishing large numbers of claims. For CTI purposes, the relevant question is not simply *"Was this target announced?"* but:

- Was the target actually reachable during the claimed period?
- Was degradation independently observed?
- Was the activity attributed by a credible third party?
- Was the effect significant or short-lived?

Europol's reporting on Operation Eastwood noted that confirmed attacks linked to the network had often been mitigated without substantial interruption. This is an example of why **claim volume and operational impact are different intelligence measures**.

### 4. Operation Eastwood validated the existence of a significant coordinated infrastructure

In July 2025, Operation Eastwood disrupted more than 100 systems worldwide and took a major part of NoName057(16)'s central infrastructure offline. Europol reported arrests, arrest warrants, searches and notifications to more than 1,000 supporters, including 15 administrators.

This provides strong independent confirmation that the ecosystem was not merely a collection of social-media claims; it relied on infrastructure and identifiable operational roles that law enforcement could target.

## Analytic assessment

**High confidence:** NoName057(16) combined ideological messaging, community mobilisation and centrally coordinated technical infrastructure.

**Moderate confidence:** Internal decision-making, individual motivations and the exact relationship between every public supporter and core operators cannot be inferred solely from public communications.

A useful model is:

`Narrative / mobilisation → target tasking → distributed execution → public claim → independent validation`

For ongoing monitoring, changes at any of these stages can provide early indicators of shifts in targeting or operational capability.

## MITRE ATT&CK

The clearest documented behaviour maps to:

- **T1498 — Network Denial of Service**
- **T1498.001 — Direct Network Flood**

Additional mappings should be campaign-specific and evidence-based rather than inferred from group identity alone.

## Intelligence gaps

- How much target selection is centrally directed versus suggested by community participants?
- Which observable channel/infrastructure changes best predict a new campaign wave?
- To what extent did post-Eastwood infrastructure and community fragmentation reduce sustained operational capacity?

## Skills demonstrated

- underground/community monitoring;
- source validation;
- claim-versus-impact analysis;
- timeline and campaign analysis;
- infrastructure-context correlation;
- confidence assessment;
- concise intelligence reporting.

## Public sources

1. Europol — *Global operation targets NoName057(16) pro-Russian cybercrime network* (16 July 2025): https://www.europol.europa.eu/media-press/newsroom/news/global-operation-targets-noname05716-pro-russian-cybercrime-network
2. Recorded Future / Insikt Group — *Anatomy of DDoSia: NoName057(16)'s DDoS Infrastructure and Targeting*: https://www.recordedfuture.com/research/anatomy-of-ddosia
3. SentinelLabs — *NoName057(16) — The Pro-Russian Hacktivist Group Targeting NATO*: https://www.sentinelone.com/labs/noname05716-the-pro-russian-hacktivist-group-targeting-nato/
4. Team Cymru — *The NoName Blog*: https://www.team-cymru.com/post/a-blog-with-noname

---

**Analyst:** Gabriele Viola  
**Portfolio:** [Back to CTI Portfolio](README.md)
