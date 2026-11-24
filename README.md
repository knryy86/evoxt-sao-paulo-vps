# Evoxt São Paulo VPS: $2.99/mo, 1Gbps Ports, All 11 Plans Compared — Which Plan Fits Brazilian Traffic, and Who Should Skip This Node (Full Price Table)

Evoxt's São Paulo region went live on **14 August 2026**. The entry plan costs **$2.99/month** for 1 core, 512MB RAM, 5GB of storage and 500GB of monthly traffic, and every plan in the region gets a **1Gbps** port. The node peers at DE-CIX São Paulo, PTT São Paulo and PTT Fortaleza, which is the part that actually matters if your visitors are in Brazil.

Two facts settle most buying decisions. Brazilian and South American audiences get a local path plus a Brazilian IPv4. Mainland Chinese audiences get whatever international routing delivers on the day, because this location is not built around China Telecom, Unicom or Mobile return paths. The rest of this page covers the full price table, which plan matches which workload, what the recurring 5% code really saves over a year, and a launch-date mix-up worth clearing up before you compare articles.

> **Quick picks**
> - Testing Brazilian latency, or running a bot/monitor: **VM-0.5 at $2.99/mo** 👉 [👉 Start with the $2.99 VM-0.5 plan](https://bit.ly/EvoXt)
> - One WordPress site, an API or a small Docker stack: **VM-1 at $5.99/mo**, which is the first plan with 2GB RAM
> - App and database on the same box: **VM-2 at $11.99/mo** for 2 cores and 4GB
> - Anything memory-hungry beyond that: VM-4 and up; most readers will never need VM-12 or VM-16

## All 11 São Paulo plans, side by side

Prices below are the standard monthly list prices for the São Paulo region. Every row includes a 1Gbps port, one IPv4, IPv6, weekly offsite backup and KVM virtualisation.

| Plan | CPU / RAM / Storage | Monthly traffic | Price/mo | Order |
| --- | --- | --- | --- | --- |
| VM-0.5 | 1 core / 512MB / 5GB | 500GB | **$2.99** | [ Order VM-0.5](https://bit.ly/EvoXt) |
| VM-0.75 | 1 core / 1GB / 10GB | 750GB | $4.99 | [ Order VM-0.75](https://bit.ly/EvoXt) |
| VM-1 | 1 core / 2GB / 20GB | 1TB | $5.99 | [ Order VM-1](https://bit.ly/EvoXt) |
| VM-1.5 | 2 cores / 2GB / 20GB | 1.5TB | $6.95 | [ Order VM-1.5](https://bit.ly/EvoXt) |
| VM-2 | 2 cores / 4GB / 30GB | 2TB | $11.99 | [ Order VM-2](https://bit.ly/EvoXt) |
| VM-3 | 4 cores / 4GB / 30GB | 3TB | $14.99 | [ Order VM-3](https://bit.ly/EvoXt) |
| VM-4 | 4 cores / 8GB / 60GB | 4TB | $23.99 | [ Order VM-4](https://bit.ly/EvoXt) |
| VM-6 | 8 cores / 8GB / 60GB | 5TB | $29.99 | [ Order VM-6](https://bit.ly/EvoXt) |
| VM-8 | 8 cores / 16GB / 80GB | 6TB | $47.99 | [ Order VM-8](https://bit.ly/EvoXt) |
| VM-12 | 16 cores / 16GB / 80GB | 8TB | $60.95 | [ Order VM-12](https://bit.ly/EvoXt) |
| VM-16 | 16 cores / 32GB / 100GB | 10TB | $95.99 | [ Order VM-16](https://bit.ly/EvoXt) |

The jump from VM-0.5 to VM-16 is roughly 32× the price for 16× the cores, 64× the RAM and 20× the traffic. There is no middle ground where the small plans suddenly become bad value; the curve is fairly even, so pick by RAM first and core count second. A single-core 2GB box handles far more real traffic than a dual-core 1GB box in most web workloads.

## What the 5% recurring code actually saves

Code **AFF145-zjcp** takes 5% off and recurs, so it applies to renewals too, not just the first invoice. That changes the math for long-lived boxes more than for test deployments.

| Plan | List price | With 5% code | Saved per year |
| --- | --- | --- | --- |
| VM-0.5 | $2.99 | $2.84 | about $1.80 |
| VM-1 | $5.99 | $5.69 | about $3.60 |
| VM-16 | $95.99 | $91.19 | about $57.60 |

On VM-0.5 the discount is nearly noise, so don't let a coupon decide whether to try the region. On VM-16 it pays for a decent chunk of a second year. Apply it at checkout rather than expecting it to appear automatically, and confirm the discount line before paying, because promo codes on this kind of console generally have expiry dates that are not published.

👉 [👉 Order a São Paulo plan with the recurring code applied](https://bit.ly/EvoXt)

One warning about annual pricing. A third-party plan directory shows VM-0.5 billed quarterly at $8.97 list and yearly at $32.29 list, which works out to roughly $2.69/month before any code. Treat those as directory figures, not confirmed official rates: I could not verify the term pricing on Evoxt's own pages, and Evoxt has changed regional pricing before. The Malaysia Premium VM-0.5 moved to $3.49/month in a May 2026 announcement, with existing VMs keeping their old price and traffic unless they were upgraded or redeployed. Budget for the possibility that a long prepay locks in today's number while a monthly plan does not.

## The launch date confusion, cleared up

Evoxt's own Telegram channel posted "New Region Live: São Paulo, Brazil" on **14 August 2026, 10:59 UTC**, quoting plans from $2.99/month and CPUs up to 6.0GHz. A third-party review published 15 August reported the data centre as live. Another article dated 24 September 2026 announced the node as "officially launched", which reads like the node's birthday but is almost certainly just that article's publication date.

Why care? Because if you are comparing coverage across sites, a September launch date makes the region look newer and less proven than it is. As of November 2026 the node has been orderable for close to three months. The internal API region code is **br-sao**, which is what you will see if you script deployments through the control panel API.

## Network: three Brazilian peering points, no China optimisation

Traffic from the São Paulo node exchanges at **DE-CIX São Paulo, PTT São Paulo and PTT Fortaleza**. That covers the two main Brazilian internet exchange ecosystems plus a northeast peering point, so local ISP traffic stays inside Brazil instead of tromboning through Miami or Europe.

Public test instances have been observed with Brazilian IPv4 addresses announced from São Paulo. IP geolocation and streaming-unlock behaviour can change, so do not buy on the assumption that a specific service will treat the address as Brazilian forever.

What you cannot do yet is check the route before paying. There is no published Looking Glass or test IP aimed at mainland Chinese users. If China access quality is part of your decision, the cheapest sane approach is to order VM-0.5 for one month, measure latency and evening peak packet loss from your actual location, and decide from that data. $2.99 is a small price for a real measurement instead of a guess.

👉 [👉 Buy the $2.99 plan to test the route yourself](https://bit.ly/EvoXt)

For anyone whose main requirement is low latency from mainland China, this is the wrong region regardless of price. Evoxt's China-optimised routing sits in its Hong Kong and Malaysia Premium network tiers, not in Brazil.

## Hardware: 6.0GHz is the promise, the CPU model is not

Evoxt's official wording is that Brazil VMs run on CPUs at up to **6.0GHz**, and the company frames high clock speed as its differentiator instead of raw core counts. That is a sensible pitch for PHP, WordPress, bots and single-threaded APIs, which is most of what a $3 VPS actually does.

The specific silicon is less settled. Public testing of a São Paulo VM-0.5 instance identified the host CPU as an **AMD EPYC Turin** processor. A separate third-party write-up describes the Brazilian data centre as using **AMD Ryzen** processors with NVMe storage. Both cannot be universally true, and neither is an official guarantee: Evoxt commits to the clock ceiling, not to a model number, and instances land on different hosts.

Read that as "expect a recent AMD core at high frequency, verify on your own instance". If a specific instruction set or CPU generation is a hard requirement for your build, check `lscpu` after provisioning and be ready to rebuild.

## Features, panel and the limits worth knowing

Every plan includes **weekly offsite backups** with one-click restore, a KVM hypervisor, IPv6, private IPs between your own VMs (traffic between them is not billed), and a rescue mode for when a boot breaks. Uptime is stated at **99.99%**. The control panel covers monitoring, IP management, a layer-3 firewall with DDoS filtering, cloning, VNC, sub-accounts and a public API. Linux and Windows are both supported.

Payment methods listed by Evoxt are credit and debit cards, PayPal, Bitcoin and USDT on Tron. One aggregator also mentions Alipay; I could not confirm that on Evoxt's own pages, so treat Alipay as unverified and have a card or crypto option ready.

On refunds, a third-party provider directory lists a 7-day refund window. Evoxt's own pages in the material I checked do not spell out the terms, so ask support before a large prepay rather than assuming the window. Note that payment-gateway fees are typically not returned, and that would matter more on a VM-16 order than on a $2.99 test box.

Hardware upgrades can be bought à la carte inside the panel, so a wrong initial choice is not fatal: extra vCPU, RAM and traffic can be added without switching plans.

👉 [👉 Check current São Paulo availability and plan options](https://bit.ly/EvoXt)

## Who should buy this, and who should not

Buy it if your users, clients or crawlers are in Brazil, or if you need a Brazilian IPv4 for a local service, a regional API endpoint, or a node in a multi-region setup where South America was the missing piece. It also works as a cheap Windows RDP box or a development environment close to Brazilian testers.

Skip it if your traffic comes mainly from mainland China. The absence of a China-optimised return path is the single most common reason people buy a Brazilian VPS and then complain about it. Being close to São Paulo does nothing for a visitor in Shanghai.

Skip the big plans, too, unless you have measured a need. VM-12 and VM-16 exist for people running multiple services or heavy concurrent workloads; a personal site or a small bot on VM-16 is $95.99/month spent on headroom you will not use.

## Ordering checklist

1. Confirm **AFF145-zjcp** still shows a 5% recurring discount in the cart before you pay.
2. Decide monthly versus prepay. Monthly costs more per month but keeps you flexible while Evoxt is still adjusting regional prices.
3. Pick the region explicitly as São Paulo (br-sao) at deploy time; the same plan sizes exist across other regions.
4. For a China-facing workload, order VM-0.5 first and measure before committing to a bigger box.
5. Ask support about the refund window if you are spending more than a test-plan amount.

## Final selection rules

Testing the region, running a monitor, a bot or a tiny API → **VM-0.5, $2.99/month**. One production website or a Docker stack that needs breathing room → **VM-1 at $5.99 or VM-1.5 at $6.95** if you want the second core. Database plus application on one host → **VM-2 at $11.99** minimum, and step to VM-4 at $23.99 when memory pressure shows up in monitoring. Everything above VM-8 is for consolidation or heavy concurrency, not for a single site.

If Brazil is where your users are, this is one of the cheaper ways to get a local 1Gbps box with weekly backups included. Start small, measure, then scale in the panel.

👉 [👉 Pick your Evoxt São Paulo plan and deploy](https://bit.ly/EvoXt)
