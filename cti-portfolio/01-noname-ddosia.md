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

## November 2026 intelligence update (reviewed 22 November 2026)

### 6. Sustained DDoS claim volume after Operation Eastwood

A public CyberXTron monitoring report covering **1–16 November 2026** recorded **85 NoName057(16)-labelled DDoS claims across 14 active days**, tied with Dark Storm Team at the top of that report's actor ranking. The same report describes overlapping claimed target lists involving Spanish and German public-sector and transport organisations. This is **third-party collected claim data**, not 85 independently confirmed outages or successful attacks. The dataset's coverage and classification limitations apply.

A separate Brandefense research dataset covering **1 January–27 October 2026** counted **578 NoName057(16) claim events** and **2,920 claimed target entries**, explicitly distinguishing posts, de-duplicated claims, listed targets and proven outcomes. These datasets are not directly additive or equivalent. They provide evidence of sustained public claim activity; neither establishes the operational effect of every listed event.

**Analytic implication:** assess narrative and tasking tempo separately from independently verified availability impact. Avoid false precision when comparing collected social posts, events, technical target configurations and incidents.

### 7. EU restrictive measures against the actor (16 November 2026)

On **16 November 2026**, the **Council of the European Union formally listed NoName057(16)** under its cyber-related restrictive measures, identifying the group as a pro-Russian hacker actor that claims attacks against government bodies, critical infrastructure and private organisations. This is an **authoritative government action**, distinct from a vendor's actor-attribution assessment or a claim made by the group.

The designation provides additional strategic context for assessing disruption, cross-border response and sanctions exposure. It does not, by itself, verify every specific attack claim or determine the individual operators behind current public channels.

### 8. New actor-branded surface-web portal reported (20 November 2026)

On **20 November 2026**, Red Hot Cyber reported a newly accessible **.com surface-web site branded NoName057(16)**. Its account describes pages for political messaging, DDoSia recruitment/gamified participation, public communications, links to messaging platforms, and a 'Tribunal' section concerning named individuals.

**Update — 22 November 2026, analyst-provided domain:** The clear-web candidate has now been identified as `noname057[.]com` (defanged intentionally). The analyst supplied the URL and a browser screenshot in this conversation. This changes the earlier status from **“unidentified .com domain reported by a third party”** to **“specific actor-branded surface-web domain reported by a third party and identified by the analyst.”** An attempt to retrieve the host from the research environment was blocked/unsuccessful; domain ownership, operator control, live reachability and equivalence to the Tor portal **remain unverified independently**. Similar slogans, branding and site sections support a possible shared presentation or mirror relationship but do not prove common infrastructure or common ownership.

**Additional primary-source corroboration (analyst-supplied, 22 November 2026):** A Telegram screenshot showing a NoName057(16)-branded channel post explicitly labels the `noname057[.]com` address as a **“mirror of our website”** and places a matching Tor/onion URL for the same `/alive/` section directly underneath. The analyst also reports that `noname057[.]com` is reachable in their own browser on 22 November 2026. This is stronger evidence for an **actor-*claimed* surface-web/Tor mirror relationship** than similarity of branding alone. It does **not** independently establish who administers the domains, that their content is identical, that the service remains available to all observers, or that any related allegation or attack claim is true. The Telegram post discusses an individual and their family; those names and allegations are deliberately excluded.

**Assessment:** **High confidence** that the analyst-provided screenshot visibly presents paired clear-web and onion links described by the poster as mirrors; **moderate confidence** in the user-reported reachability at observation time; **low/unestablished confidence** in independently verified infrastructure/owner attribution or persistent technical equivalence. The date is the analyst's **submission/observation date**, not an independently established post-publication timestamp.

**Safe-handling note:** This public portfolio does not provide a clickable link to the actor-branded web property. No downloads, contact invitations, personal-data listings or named persons from the 'Tribunal' section are included.

**Source classification: third-party reporting of a purported actor-controlled web property.** The appearance and branding of the portal, as described in the report, should not be mistaken for independent verification of site ownership, recruitment success, the group's self-advertised capabilities (including phishing, malware or ransomware), any leak claims, or operational impact. I have **not independently verified the new domain's infrastructure or contents for this update**.

The new portal is **not the same as witha.name**, which is an independent DDoSia technical-monitoring service. The reported development matters because actor-facing communication appears to be expanding beyond Telegram and Tor to a more discoverable public web presence, potentially increasing recruitment reach and propaganda resilience. The portal's personally identifying 'Tribunal' material is **not reproduced or linked** here.

### Source supplement — actor-branded communications directory (analyst-supplied, 22 November 2026)

An analyst-supplied transcription of a purported **NoName057(16)-branded Tor portal** lists an actor-labelled main Telegram channel, a DDoSia project channel, multiple language-specific Telegram communities (English, Spanish, Italian, German and French), a backup channel, and an Element/Matrix room. Its navigation also advertises political messaging, media, DDoSia software, a 'Tribunal' section, news and alleged data leaks.

**Evidence class:** analyst-provided page transcription / actor-branded primary-source material. These observations **have not been independently authenticated** by an investigator-controlled crawl, verified operator announcement, or technical attribution. The existence of a navigation item, recruitment offer or leak claim is not proof of actor control, real-world impact, or operational capability.

**Analytic significance:** actor-labelled multilingual channels, cross-platform communication and redundant contact points are potentially useful signals of audience expansion, propaganda continuity and recovery after disruption. Future monitoring should record changes in claims and access paths separately from verified technical incidents.

The private evidence index includes sanitized source-context notes. **No live onion URLs, invite tokens, downloads, named individuals or victim data are reproduced here.** This actor-branded portal must not be confused with independent telemetry at witha.name.

### 9. Broader claims: collaboration and industrial-system context

A **4 November 2026** Rai News report describes a *jointly claimed* refrigeration-system incident by NoName057(16) and Z-Pentest. DarkOwl's November 2026 assessment additionally notes increased amplification of allied groups and claims concerning ICS/CCTV environments. These observations justify tracking collaboration and changes in messaging; **a joint claim is not proof of independently confirmed compromise**, and an allied group's claimed technique is not automatically attributable to every NoName057(16) campaign.

**Updated assessment (22 November 2026)**

- **High confidence:** The actor remains publicly associated with a substantial DDoS claim ecosystem, and EU authorities officially listed NoName057(16) on 16 November 2026.
- **Moderate confidence:** Reported new surface-web branding and allied-group messaging indicate an effort to diversify public reach and mobilisation.
- **Low confidence / not established:** Actual incident success rates, direct ownership of the reported domain, completeness of external claim datasets, and expanded offensive capabilities claimed by the actor itself.

**Collection and OPSEC note:** This update combines independently published desk research with a clearly labelled analyst-supplied portal transcription, **not an independently authenticated investigator-controlled capture**. No credentials, source personas, personal-data lists, current target configurations or links to actor recruitment/download infrastructure are included.

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
7. Council of the EU — *Russia's FIMI and malicious cyber activities: Council imposes sanctions* (16 November 2026): https://www.consilium.europa.eu/en/press/press-releases/2026/11/16/russia-s-fimi-and-malicious-cyber-activities-council-imposes-sanctions-on-30-individuals-and-two-entities/
8. CyberXTron — *Hacktivism Watch, 1–16 November 2026*: https://cyberxtron.com/resources/blogs/hacktivism-watch-the-biweekly-pulse-november-1-16-2026-8333
9. Brandefense — *Hacktivism and DDoS: What the Claim Posts Record* (30 October 2026): https://brandefense.io/wp-content/uploads/cybercrime-report-2026/hacktivism-ddos/hacktivism-ddos-report-2026.html
10. Red Hot Cyber — *NoName057(16) launches actor-branded clear-web .com site* (20 November 2026): https://www.redhotcyber.com/post/gli-hacker-filorussi-di-noname05716-sbarcano-sul-clear-web-aperto-il-sito-com/
11. DarkOwl — *NoName057(16) Telegram Activity Assessment* (November 2026): https://www.darkowl.com/blog-content/noname05716-telegram-activity-assessment/
12. Rai News — *Two groups claim refrigeration-system attacks* (4 November 2026): https://www.rainews.it/articoli/2026/11/due-gruppi-di-hacker-filorussi-rivendicano-gli-attacchi-ai-frigoriferi-7b449272-1283-4caa-8e6e-f7afabbe9035.html

---

**Analyst:** Gabriele Viola  
**Portfolio:** [Back to CTI Portfolio](README.md)
