---
title: "Gyazo's 174 Million Deleted Files Are Still Out There — And That's the Real Story"
excerpt: "A breach at Gyazo exposed metadata for 174 million images users thought they had deleted. Deletion was never the same as erasure."
lang: en
date: 2026-09-26
canonical_url: https://longdrive.cc/blog/gyazo-1-74-1b4f4d
---

## The number that matters isn't the breach. It's the 174 million.

Helpfeel's second disclosure on September 25 about the Gyazo breach added a detail that got less attention than it deserved: roughly 174 million records of metadata from images that users had *already deleted* were also exposed. Not current files. Discarded ones. The images people removed from their accounts, presumably because they no longer wanted them to exist.

That figure reframes the incident. The headline is an unauthorized access case at a popular screenshot-sharing service. The more uncomfortable finding is that "delete" behaved the way it almost always does on conventional cloud infrastructure — as a change in visibility, not a change in existence.

## Deletion is a UI convention, not a storage guarantee

Most cloud services implement deletion the way a filing clerk would: they move the record to a place you can't see, and eventually someone gets around to shredding it. Sometimes that happens quickly. Often it doesn't. Backups, replicas, cold storage tiers, and disaster-recovery snapshots mean a single "deleted" object can persist across multiple systems for months or years, each with its own access surface.

This is not a bug at Gyazo specifically. It is the default architecture of the entire subscription-cloud model, and it has produced a long line of uncomfortable disclosures. In 2019, a security researcher found that years of deleted photos and videos remained accessible on a photo-hosting service's servers. In 2022, a major social platform was reported to have retained deleted user data in analytics pipelines. The pattern repeats because the economics of cloud storage reward keeping copies — replication is cheap, and re-deriving data you threw away is expensive.

So when a breach occurs, the blast radius is not "the data you currently have stored." It is everything the provider ever retained, including the parts you believed you had removed. Users of Gyazo learned that their deleted image metadata was still sitting in a system that could be reached by someone else.

## Metadata is the part people underestimate

The instinct is to treat metadata as harmless — just timestamps and filenames. That instinct is wrong. Image metadata routinely includes upload times, device identifiers, geolocation tags, account linkage, and sometimes the original filename, which can itself be revealing ("passport_scan_2023.jpg" is not a neutral string).

A set of 174 million metadata records, correlated across accounts and time, is a behavioral map. It tells you who was active when, what kinds of documents they were handling, and where they were. It doesn't require the pixels to be damaging.

This is also why "we only lost metadata" is a weaker reassurance than it sounds. For investigative journalists, activists, or anyone whose threat model includes correlation rather than direct exposure, metadata is frequently the more sensitive layer.

## The economics quietly push against true deletion

There is a structural reason this keeps happening. Subscription storage businesses are priced to cover ongoing costs: servers, replication, bandwidth, and the operational overhead of keeping a large fleet of disks healthy. Retention of deleted data is, in that model, a cost center with no revenue attached. It gets minimized, not eliminated.

Contrast that with prepaid, permanent storage architectures such as Arweave, where a one-time fee funds storage in perpetuity across a decentralized network. The incentive structure is different in a way that matters here: what you upload is what persists, and there is no separate "recycle bin" holding your discarded files in a state that can later leak. On Long Drive, the cloud drive built on Arweave by Supercomputing International (Hong Kong), files are stored once and remain, with optional client-side AES-256-GCM encryption so that the private key — and therefore the content — stays with the user. The platform cannot read what it cannot decrypt.

That is not a claim that any system is breach-proof. It is a claim about a different failure mode. The Gyazo incident is less about a single intrusion than about a storage model in which deletion was never really deletion.

## The question to ask your storage provider

The useful takeaway from 174 million deleted records is not "change your password." It is a question worth asking of every service holding your data: when I delete something, what actually happens to it — and for how long?

Most providers cannot answer that precisely, because their own infrastructure cannot either. Data that is meant to be gone should be gone by design, not by cleanup policy. Until that becomes the norm, the safest assumption is the one the Gyazo disclosure just demonstrated: the files you deleted are still somewhere, and someone may still be able to reach them.

---
*Cross-posted from [Long Drive Blog](https://longdrive.cc/blog) — permanent storage on Arweave. 本文由超算国际（香港）自动发布。*
