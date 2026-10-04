# rayobyte pricing: what you pay per GB and per IP, and when a flat per-IP rate wins

Rayobyte doesn't have a price. It has a price sheet.

Search for its pricing and you'll run into four or five different numbers, all technically correct. That's because Rayobyte sells residential, datacenter, ISP/static residential, and mobile proxies, plus a scraping API, and those products bill in different units. Residential is per gigabyte. Datacenter and ISP are per IP per month. The mobile and API lines go back to per gigabyte. Pick the wrong unit for your workload and the cheapest headline rate on the page stops mattering.

Here's how the published rates actually stack up, where the discounts really sit, and the situation where a per-IP residential provider like 9Proxy ends up cheaper for the same job.

## Rayobyte's published rates at a glance

These are the rates Rayobyte publishes on its own pricing page, as recorded by third-party price trackers in August 2026. Rayobyte reshuffles its volume bands from time to time, so treat this as a shape rather than a lock.

| Product | Billing unit | Published entry rate | Where the rate drops |
| --- | --- | --- | --- |
| Residential (rotating) | Per GB | $3.50/GB, 1–49 GB, pay as you go | $2.00/GB at 50–249 GB, $1.50/GB at 250–999 GB, $0.70/GB at 1,000–4,999 GB |
| ISP / static residential | Per IP per month | $5/IP, 5-IP minimum | $4.80/IP mid tier, $4.60/IP at 1,000 IPs |
| Datacenter (dedicated or semi-dedicated) | Per IP per month | $2/IP | From $1/IP on shared semi-dedicated IPs |
| Datacenter (rotating) | Per GB | $0.30/GB, 1–50 GB | Roughly $0.25/GB in the low hundreds of GB |
| Mobile | Per GB | $1.25/GB | Custom at high volume |
| Scraping API / Web Unblocker | Per GB | $6/GB | $2.50/GB at 501 GB–1 TB |

One thing to clear up immediately: if you find a review quoting $15/GB for Rayobyte residential, look at the date. That number shows up in write-ups from 2024 and 2025 and hasn't matched the pricing page for a while.

## Residential proxies: the per-GB bands do all the work

The residential line is the one most people searching "rayobyte pricing" actually care about, and it's built like a volume ladder.

You start at $3.50 per GB with a pay-as-you-go purchase and no commitment. Between 50 and 249 GB the rate drops to $2.00. Between 250 and 999 GB it's $1.50. The real discount shows up at 1,000 GB, where it falls to $0.70 per GB, and the "from $0.50/GB" figure on marketing pages only exists at 5,000 GB per month and above.

Run those through a calculator and the shape becomes obvious:

- 50 GB at $2.00/GB — $100
- 200 GB at $2.00/GB — $400
- 500 GB at $1.50/GB — $750
- 1,000 GB at $0.70/GB — $700
- 5,000 GB at $0.50/GB — $2,500/month

That 1,000 GB step is the interesting one. Your per-GB cost drops by more than half, and the monthly bill only sits about $50 above the 500 GB tier. If you're anywhere near 700–800 GB a month, buying the 1,000 GB band is straightforwardly cheaper than buying the smaller one.

There's a second detail that matters more than most comparison articles mention. One-time residential bandwidth doesn't expire. Rayobyte's own site puts it this way:

> "The residential bandwidth you purchase doesn't expire. We offer one-time purchases with no commitment. Once you buy 50 GB, you have access to that 50 GB until you use it up."

So the $2.00/GB band isn't a monthly subscription you have to drain in 30 days. It's a balance. If your projects come in waves, you're not automatically throwing away the tail of the package, which is how a lot of "cheap" per-GB providers actually end up expensive.

## ISP and datacenter: now you're paying per IP

Different product, different unit, different psychology.

ISP proxies (sometimes called static residential) start at $5 per IP per month with a 5-IP minimum, drifting to around $4.80 on mid tiers and $4.60 per IP at the 1,000-IP level. Those IPs come with unmetered bandwidth and roughly 1 Gbps speeds, and they're the honest answer for work where the IP has to stay the same for weeks: account management, SEO rank tracking, ad verification, anything where a rotating IP triggers a security check.

Datacenter proxies are cheaper per unit, from $2 per IP for dedicated addresses and from $1 per IP on semi-dedicated shared ones, billed monthly. The rotating datacenter product flips back to per-GB billing at $0.30/GB, which is the cheapest per-gigabyte number anywhere on Rayobyte's sheet.

Worth knowing before you budget: ISP static IPs don't come with a free trial. AIMultiple's review of static residential providers notes Rayobyte offers a 2-day money-back window instead. Two days is enough to confirm the IPs connect, not enough to judge a two-week scraping job.

## The costs that aren't on the price page

Three things quietly change the total, and none of them are in the headline rate.

**Commitment.** The low per-GB bands assume monthly volume commitments. Getting to $0.70/GB means committing to 1,000 GB a month, not buying 1,000 GB once. That's the gap between the number on the marketing page and the number on your card.

**Billing period.** ISP and datacenter are monthly per-IP products. If you need 50 static IPs for a three-week project, you're paying for the month regardless.

**The gap between "want to try" and "buying."** Rayobyte's entry for residential is a genuine pay-as-you-go purchase, which is a reasonable trial substitute. On static ISP, it's a 2-day refund window.

None of that is unreasonable. Rayobyte has been in the proxy business since its Blazing SEO days and rebranded in 2022; it publishes its bands openly, which is more than a lot of providers manage. The point is that the model has a shape, and if your workload doesn't match the shape, you're paying for a discount you can't reach.

## Per-GB pricing punishes the wrong kind of workload

Per-GB billing has one structural quirk: your bill scales with bytes, and bytes aren't the same thing as work completed.

A scraper with a bug in its retry loop burns bandwidth and produces nothing. Pages with heavy images or JavaScript payloads cost multiples of what a clean HTML endpoint costs. A run that gets rate-limited halfway through still pays for every request it made. When bandwidth usage is predictable, this is fine and often cheap. When it's not, per-GB pricing pushes the risk of your own code onto your invoice.

That's the case where a per-IP model with unlimited bandwidth is worth a serious look. Which brings us to 9Proxy.

## 9Proxy's pricing, in full

9Proxy sells residential proxies only, so it isn't a like-for-like replacement for everything on Rayobyte's sheet. What it does differently is the billing model. You buy a balance, not a subscription, and the balance comes in three shapes:

- **Residential by IP** — you pay per IP with unlimited bandwidth while an IP is active. Unused IPs never expire.
- **Residential by GB** — you pay per gigabyte and generate unlimited proxy endpoints, with 180-day validity (unlimited on Enterprise).
- **Bundles** — IPs plus traffic in one package for mixed workloads.

The nuance people miss on IP-based plans: an IP isn't a monthly seat. The documentation describes it as one activation per IP forwarded, with each IP living anywhere from a few hours up to about 24 hours on natural residential uptime, and no bandwidth meter running during that window. So a 100-IP pack is 100 activations, and it never expires if you don't use them all.

Here's the IP-based ladder as it stands after the June 2026 adjustment (GB-based prices were left untouched):

| IP package | Price per IP | Total | Purchase |
| --- | --- | --- | --- |
| 100 IPs | $0.24 | $24 | [ Get the 100-IP pack](https://bit.ly/9-Proxy) |
| 500 IPs | $0.144 | $72 | [ Get the 500-IP pack](https://bit.ly/9-Proxy) |
| 1,000 IPs + 500 bonus | $0.084 | $126 | [ Get the 1,000 + 500 IP pack](https://bit.ly/9-Proxy) |
| 2,500 IPs | $0.084 | $210 | [ Get the 2,500-IP pack](https://bit.ly/9-Proxy) |
| 5,000 IPs | $0.072 | $360 | [ Get the 5,000-IP pack](https://bit.ly/9-Proxy) |
| 15,000 IPs | $0.048 | $720 | [ Get the 15,000-IP pack](https://bit.ly/9-Proxy) |
| 25,000 IPs | $0.035 | $863 | [ Get the 25,000-IP pack](https://bit.ly/9-Proxy) |
| 50,000 IPs | $0.029 | $1,438 | [ Get the 50,000-IP pack](https://bit.ly/9-Proxy) |
| 100,000 IPs (Business) | $0.023 | $2,300 | [ Get the 100,000-IP business pack](https://bit.ly/9-Proxy) |
| 200,000 IPs (Business) | $0.021 | $4,140 | [ Get the 200,000-IP business pack](https://bit.ly/9-Proxy) |
| 500,000 IPs (Business) | $0.018 | $8,625 | [ Get the 500,000-IP business pack](https://bit.ly/9-Proxy) |

The GB-based side, which is the direct comparison to Rayobyte's residential line:

| GB package | Price per GB | Total | Validity | Purchase |
| --- | --- | --- | --- | --- |
| 5 GB | $3.00 | $15 | 180 days | [ Get the 5 GB pack](https://bit.ly/9-Proxy) |
| 50 GB + 5 bonus | $2.10 | $105 | 180 days | [ Get the 50 GB pack](https://bit.ly/9-Proxy) |
| 100 GB | $1.50 | $150 | 180 days | [ Get the 100 GB pack](https://bit.ly/9-Proxy) |
| 200 GB | $1.00 | $200 | 180 days | [ Get the 200 GB pack](https://bit.ly/9-Proxy) |
| 1,000 GB | $0.80 | $800 | 180 days | [ Get the 1,000 GB pack](https://bit.ly/9-Proxy) |
| 2,000 GB | $0.75 | $1,500 | 180 days | [ Get the 2,000 GB pack](https://bit.ly/9-Proxy) |
| 3,000 GB (Enterprise) | $0.72 | $2,160 | No expiry | [ Get the 3,000 GB enterprise pack](https://bit.ly/9-Proxy) |
| 6,000 GB (Enterprise) | $0.70 | $4,200 | No expiry | [ Get the 6,000 GB enterprise pack](https://bit.ly/9-Proxy) |
| 10,000 GB (Enterprise) | $0.68 | $6,800 | No expiry | [ Get the 10,000 GB enterprise pack](https://bit.ly/9-Proxy) |

And the three bundles, for teams that need sticky sessions and throughput in the same invoice:

| Bundle | What's in it | Price | Purchase |
| --- | --- | --- | --- |
| Starter | 100 IPs + 5 GB | $30 | [ Get the Starter bundle](https://bit.ly/9-Proxy) |
| Popular | 1,500 IPs + 50 GB | $180 | [ Get the Popular bundle](https://bit.ly/9-Proxy) |
| Pro | 5,000 IPs + 500 GB | $720 | [ Get the Pro bundle](https://bit.ly/9-Proxy) |

Two structural facts about 9Proxy that are genuinely different from Rayobyte's residential line. First, GB balances carry 180-day validity rather than 30 days, and Enterprise balances don't expire at all, which matters if your usage is lumpy. Second, endpoint generation is unmetered on GB plans: rotating through the whole pool doesn't cost extra IP fees, you just spend traffic.

The network itself is advertised at 20 million-plus residential IPs across 90-plus countries. Independent write-ups put success rates in the high nineties on mainstream targets, and the platform is a cheap entry point rather than a high-performance pick. ProxyLook's directory scores it 3.9 out of 5; Geekflare's 2026 review describes it as a budget residential provider worth using if the per-IP model fits your workload.

## Running the numbers on a real workload

Say you're scraping about 200 GB a month against mid-difficulty targets, and you need somewhere around 40 concurrent sessions.

**On Rayobyte residential:** 200 GB falls into the 50–249 GB band at $2.00/GB, so about $400/month. Drop that volume to 150 GB and you're at $300. Commit to 1,000 GB and the rate falls to $0.70/GB, but you're now paying $700/month for bandwidth you may not use.

**On 9Proxy GB:** the 200 GB package is $200 one-time at $1.00/GB, valid 180 days. If you actually burn 200 GB a month, you're buying roughly one package a month, so about $200/month. The catch is real: it's a balance, and if you stop working, the clock still runs.

**On 9Proxy by IP:** 40 concurrent sessions running through a full day is roughly 40 activations. A 100-IP pack costs $24 and covers more than two days at that concurrency, with unlimited bandwidth while each IP is live. Do the arithmetic across a month of steady scraping and the per-IP model is dramatically cheaper per unit of work — but only if your sessions genuinely fit inside that few-hours-to-a-day window. Long-running jobs pinned to one IP for a week are not this product's job.

That last sentence matters. The per-IP model isn't "unlimited everything for $24." It's unlimited bandwidth inside a short-lived activation. Match the workload and it's very efficient. Mismatch it and you're re-buying activations mid-job.

## Where Rayobyte still wins

There are workloads where 9Proxy isn't the alternative, and it's worth being blunt about them:

- **Static ISP or dedicated datacenter IPs.** 9Proxy doesn't sell either. If you need an IP that stays identical for a month, Rayobyte's $4.60–$5.00 per IP line is the product you want.
- **Predictable, high-volume bandwidth with a per-GB budget.** If you commit to 1,000 GB or more every month and your traffic is steady, Rayobyte's $0.70/GB band and above is a straightforward volume deal.
- **US-heavy dedicated IP stock.** Rayobyte's dedicated inventory skews to US locations, which is a real advantage for geo-specific work.
- **Unblocking hard targets.** The Web Unblocker API at $2.50–$6.00/GB is a different tool from raw residential proxies.

## Quick decision guide

- Bandwidth unpredictable, sessions short, projects intermittent → 9Proxy's IP-based packs. You stop paying for retries and heavy pages.
- Steady monthly volume above ~700 GB, per-GB budget → Rayobyte's 1,000 GB band is the cheaper ladder step.
- Same IP for weeks → Rayobyte ISP or datacenter. No comparison here.
- Testing before committing → 9Proxy's GB packages start at $15, and Rayobyte's residential entry is genuine pay-as-you-go with non-expiring bandwidth.
- Team with mixed needs → a 9Proxy bundle covers sticky IP access and traffic without two invoices.

## A few questions people actually ask

**Is Rayobyte priced per GB or per IP?**
Both, depending on the product. Residential and mobile are per GB. ISP and datacenter are per IP per month. The scraping API is per GB.

**Does Rayobyte's residential bandwidth expire?**
No. Their site states one-time residential purchases don't expire and carry no commitment, so an unused balance stays available. Low per-GB rates, on the other hand, assume monthly volume commitments.

**Is there a Rayobyte free trial?**
There's a money-back window rather than a trial. AIMultiple notes Rayobyte doesn't offer a free trial on static ISP proxies and provides a 2-day money-back guarantee instead.

**Is 9Proxy cheaper than Rayobyte?**
For GB-based residential traffic, yes at most volume points: $1.00/GB at the 200 GB package against Rayobyte's $2.00/GB in the same 50–249 GB band. For IP-based work with unlimited bandwidth, the per-unit cost is far lower, but the tradeoff is a short-lived activation window rather than a monthly seat.

**Why do some articles still list Rayobyte residential at $15/GB?**
Those figures come from 2024–2025 write-ups. The rate recorded from Rayobyte's own pricing page in August 2026 is $3.50/GB at entry. Their bands have moved more than once.

**Can I mix models?**
You can, and for some teams it's the right call: Rayobyte for static ISP identities, 9Proxy for the rotation-heavy scraping that would otherwise burn a per-GB budget.

## The short version

Rayobyte's pricing rewards volume commitment and punishes anything that looks like guesswork. If you know your monthly gigabytes, their ladder is transparent and the 1,000 GB band is where it starts making sense. If you mostly know how many parallel sessions you need and not how much traffic they'll chew through, a per-IP model with unlimited bandwidth puts the meter on the other side of the table.

[👉 Check 9Proxy's current package list and prices](https://bit.ly/9-Proxy) before you commit to a bandwidth band you might not fill.
