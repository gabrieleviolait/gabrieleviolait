# Case Study 01 — NoName057(16) / DDoSia
## Monitoring an evolving pro-Russian hacktivist DDoS ecosystem

**Focus:** Hacktivism · Telegram monitoring · DDoS infrastructure · OSINT/CLOSINT · Threat-actor tracking  
**Research type:** Independent, passive CTI research  
**Analyst background:** Historical passive observation of actor-associated Telegram/community sources, combined with current monitoring of independent technical telemetry and public monitoring infrastructure.

> **Publication note:** This public case study is sanitized. It does not publish live onion addresses, private invitations, research identities or operationally useful infrastructure details.

## Intelligence Requirement

**How does NoName057(16) translate ideological messaging and community mobilisation into coordinated DDoS activity, and which observable signals remain useful when the actor's communication channels change, fragment or disappear?**

## Collection approach

The case separates five evidence types:

1. **Actor-controlled communications** — useful for messaging, claimed targets and mobilisation.
2. **Technical infrastructure research** — useful for understanding DDoSia delivery, C2 architecture and target distribution.
3. **Independent technical telemetry** — useful for maintaining visibility when actor-controlled channels become unstable or migrate.
4. **Independent impact reporting** — useful for checking whether claims correspond to observable disruption.
5. **Law-enforcement reporting** — useful for validating structure, scale and disruption outcomes.

An actor claim is therefore recorded as a **claim** until independently corroborated.

## Key findings

### 1. Telegram was part of the operational ecosystem, not only a propaganda channel

NoName057(16) used public and community-facing channels to communicate political narratives, announce targets and mobilise supporters. Early SentinelLabs research documented the group's Telegram presence, a volunteer-fuelled DDoS participation model and DDoSia tooling across multiple operating systems.

This made messaging channels useful CTI sources for:

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

### 5. Source migration changes the collection strategy

A useful CTI lesson from longitudinal monitoring is that **visibility must survive the loss or migration of a single source**.

By September 2026, my monitoring workflow no longer depended only on Telegram/community channels. I also followed independent technical monitoring sources that surface DDoSia configuration changes on the surface web and through federated social infrastructure. Public examples include **witha.name** and the CIRCL-hosted **@NoName57Bot** Mastodon account.

These are **not official NoName057(16) channels**. Their value is different: they provide independent technical telemetry that can be compared against historical actor messaging, public claims and external reporting.

A resilient collection path therefore looks more like:

`Actor messaging → independent telemetry → public technical feeds → archived / alternative access → cross-source validation`

**Current analyst observation — 17 September 2026:** active DDoSia-related configuration monitoring was still being published through these independent sources. Target details and access-enabling information are intentionally omitted from this public portfolio.

This matters because threat actors can change platforms, lose channels, fragment their communications or deliberately manipulate their public narrative. A CTI workflow should preserve continuity even when the original source disappears.

## Analytic assessment

**High confidence:** NoName057(16) combined ideological messaging, community mobilisation and centrally coordinated technical infrastructure.

**High confidence:** Independent technical monitoring can provide continuity of visibility after disruption or channel migration, but it must be distinguished from actor-controlled communications.

**Moderate confidence:** Internal decision-making, individual motivations and the exact relationship between every public supporter and core operators cannot be inferred solely from public communications or technical feeds.

A useful model is:

`Narrative / mobilisation → target tasking → distributed execution → public claim → independent telemetry / validation`

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
- Which independent telemetry signals are most reliable for distinguishing recycled claims from genuinely new DDoSia tasking?

## Skills demonstrated

- underground/community monitoring;
- resilient multi-source collection;
- source validation;
- claim-versus-impact analysis;
- technical telemetry correlation;
- timeline and campaign analysis;
- infrastructure-context correlation;
- confidence assessment;
- concise intelligence reporting.

## Public sources

1. Europol — *Global operation targets NoName057(16) pro-Russian cybercrime network* (16 July 2025): https://www.europol.europa.eu/media-press/newsroom/news/global-operation-targets-noname05716-pro-russian-cybercrime-network
2. Recorded Future / Insikt Group — *Anatomy of DDoSia: NoName057(16)'s DDoS Infrastructure and Targeting*: https://www.recordedfuture.com/research/anatomy-of-ddosia
3. SentinelLabs — *NoName057(16) — The Pro-Russian Hacktivist Group Targeting NATO*: https://www.sentinelone.com/labs/noname05716-the-pro-russian-hacktivist-group-targeting-nato/
4. Team Cymru — *The NoName Blog*: https://www.team-cymru.com/post/a-blog-with-noname
5. Independent DDoSia monitoring — witha.name: https://witha.name/
6. CIRCL Mastodon — @NoName57Bot: https://social.circl.lu/@NoName57Bot

---

**Analyst:** Gabriele Viola  
**Portfolio:** [Back to CTI Portfolio](README.md)
