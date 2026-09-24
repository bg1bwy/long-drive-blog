---
title: "When AI Companies Spy on Each Other, Your Data Is the Casualty"
excerpt: "China's probe into DeepSeek and Moonshot over Claude data leaks exposes a deeper problem: your conversations are training data, and they may not be stored where you think."
lang: en
date: 2026-09-24
canonical_url: https://longdrive.cc/blog/china-probes-deepseek-and-moonshot-over-alleged-data-leaks-t-b92cdd
---

Anthropic's accusation that DeepSeek and Moonshot secretly routed millions of user exchanges through Claude to train their own models has triggered an investigation by China's internet regulator. The number that matters here isn't the millions of exchanges—it's the word "secretly." If the allegations hold, users on both platforms were unwitting participants in a data pipeline they never agreed to, feeding their conversations into systems they didn't choose.

The incident is a stress test for a question the AI industry has largely dodged: when you type into a chatbot, who actually owns the exchange, and where does it live?

## The Illusion of the Walled Garden

Most AI companies present themselves as self-contained ecosystems. You use their model, their servers, their terms of service. But the reality is messier. Startups routinely use third-party APIs to bootstrap capabilities—fine-tuning, evaluation, or even basic inference—while marketing themselves as fully independent. DeepSeek and Moonshot are both Chinese firms subject to data localization rules, which makes the alleged routing through Anthropic's Claude particularly sensitive. It's not just a technical shortcut; it's a jurisdictional contradiction. Data that should stay inside China's regulatory perimeter was allegedly touching U.S. infrastructure.

For users, the lesson is straightforward: the company logo on the chat interface tells you almost nothing about where your data travels. The supply chain of modern AI is opaque by design, and opacity is where leaks breed.

## Your Conversations Are the Product

There's a reason AI companies fight so hard for user data. A single conversation is low value, but millions of them form a training corpus that can cost tens of millions of dollars to assemble otherwise. When Anthropic accused its rivals of routing exchanges through Claude, the implicit charge was theft of that corpus—not just a terms-of-service violation, but a competitive moat breach.

This dynamic isn't new. In 2023, Twitter threatened to sue Microsoft over alleged misuse of its API data for AI training. Reddit controversially monetized its user posts to Google for the same purpose. The pattern is consistent: platforms treat user-generated data as an asset, and the boundaries around that asset are enforced—or ignored—based on leverage, not ethics.

The uncomfortable implication for anyone using AI tools is that your conversations may be training data, and they may be stored indefinitely, in places you never intended. Deleting a chat from your history doesn't delete it from a training pipeline, a backup server, or a third-party API log.

## The Real Cost of "Free" Storage

Cloud storage economics reinforce this problem. Subscription models—$10 per month for 2TB, say—create a recurring revenue stream that incentivizes providers to keep your data as long as possible. The longer it sits, the more opportunities for it to be accessed, breached, or repurposed. And when a provider changes ownership or pivots its business, your data becomes a line item in an acquisition, not a personal archive.

An alternative model exists: one-time payment for permanent storage, where the economics align with data persistence rather than data harvesting. Arweave, a decentralized storage network, uses this approach—you pay once, and the file is stored across a distributed network with the fee prepaid for centuries. Long Drive, a cloud drive built on Arweave and operated by Supercomputing International in Hong Kong, applies this to consumer and business archives. Files can be client-side encrypted with AES-256-GCM, meaning the private key stays with the user; even the platform can't read the contents. For documents, photos, or corporate records that need to outlive the next product cycle, that's a different contract than the subscription model offers.

## What the DeepSeek Probe Should Teach Us

The investigation into DeepSeek and Moonshot will likely produce fines, policy changes, and a round of public statements about data governance. But the deeper issue is structural. As long as user data is the fuel for AI training, companies will have incentives to route it, copy it, and retain it—sometimes across borders and legal boundaries.

For individuals and organizations, the practical takeaway is to treat every AI conversation as potentially permanent and potentially public. Assume it will be stored somewhere you don't control. Then decide what you're willing to type. The alternative—demanding verifiable, encrypted, user-controlled storage—isn't a technical fantasy. It's a design choice that some platforms are already making. The question is whether users will start treating that choice as a requirement rather than a feature.

---
*Cross-posted from [Long Drive Blog](https://longdrive.cc/blog) — permanent storage on Arweave. 本文由超算国际（香港）自动发布。*
