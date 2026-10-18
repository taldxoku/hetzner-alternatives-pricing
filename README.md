# hetzner alternatives: real prices, traffic limits and region coverage compared — and how to pick the right provider for your workload

The search for Hetzner alternatives suddenly makes a lot more sense this year, and the trigger is easy to date. Hetzner raised prices twice in quick succession: the first adjustment took effect on April 1 and covered existing servers as well as new orders, the second landed on June 15 for new orders and resizes. The CPX22 cloud plan went from €7.99 to €19.49 per month — more than doubled — the CX23 rose from €3.99 to €5.49 (about 38% up), and the US CPX11 jumped from €5.99 to €17.49, close to triple. Hetzner's budget Cost-Optimized line, meanwhile, is currently marked as not available.

Price is only part of the story. Hetzner runs six regions, three of them in Europe (Falkenstein, Nuremberg and Helsinki), so if your users sit in South America, Africa or most of Asia, distance is a problem no pricing change can fix. New accounts can also run into identity checks or credit-card prepayment requests before approval, and support is email-only — no phone, no live chat.

The short version for anyone in a hurry: **Vultr** is the closest like-for-like swap, with the same self-service, hourly-billed model, a $3.50 entry plan with IPv4 included, and 33 regions across six continents. DigitalOcean is the pick when managed databases and developer tooling matter more than raw price, OVHcloud when unmetered EU traffic matters, Contabo or netcup when you're chasing RAM per euro inside Europe. Hetzner still wins some of these comparisons, and this article says exactly where.

> **If you just want the answer:** most people replacing Hetzner end up on **Vultr**, because it keeps the pick-a-plan-and-deploy simplicity while adding regions Hetzner doesn't operate. Entry pricing is $3.50/month with an IPv4 address, or $2.50 for an IPv6-only instance, billed hourly and capped at the monthly rate. 👉 [Check Vultr's current plans and regions](https://bit.ly/VulTR)
>
> One honest caveat before you move: if your workload leans on Hetzner's 20 TB monthly traffic allowance in Europe, an entry plan elsewhere can cost you more once overage billing starts. That case gets its own section below.

## Why Hetzner customers are shopping around right now

Three things pushed people toward alternatives: price, coverage and signup friction.

The price changes are the loudest. What makes them sting a little more is how the quotes work: Hetzner's listed prices exclude VAT and an IPv4 address, while the entry prices from the providers compared below include one. On a like-for-like headline, the gap opened by the increases is wider than the sticker prices suggest.

Availability is the second trigger. Popular dedicated-server and cloud types have periodically sold out or sat behind a "currently unavailable" banner for weeks, and Hetzner's own cost-optimized cloud line is flagged as unavailable right now. Teams that need a second machine tomorrow don't have the luxury of waiting.

The third is onboarding. Hetzner's fraud-prevention documentation says it may request a government ID or a credit-card prepayment before processing an order, and incomplete details can get an account rejected. For a legitimate but unusual workload, that review process can cost days.

## The main Hetzner alternatives at a glance

| Provider | Best at | Entry price | Main catch |
| --- | --- | --- | --- |
| Hetzner (baseline) | Cheap EU compute with big traffic allowances | CX23 now €5.49/mo ex VAT (was €3.99) | Quotes exclude VAT and IPv4; cost-optimized line unavailable; email-only support |
| Vultr | Region coverage at a low price floor | $3.50/mo with IPv4 ($2.50 IPv6-only) | Backups add ~20% of instance cost; snapshots and overage traffic billed per GB |
| DigitalOcean | Developer experience and managed services | $4/mo | Entry plan carries just 512 MiB of RAM |
| Akamai Cloud (Linode) | Generous included transfer for the price | $5/mo | Reviewer reports flag slower support than hyperscaler premium tiers |
| OVHcloud | Unmetered EU traffic and bundled anti-DDoS | From €3.81/mo ex VAT (12-month upfront) | Cheapest rate requires paying 12 months up front |
| netcup | Low RAM cost in Europe | €8.26/mo ex VAT (12-month term) | Contract pricing — 1, 12 or 24 months |
| UpCloud | Cheap EU plans with hourly billing | €3/mo | Hourly billing capped at 28 days per month |
| Scaleway | No egress fees and French sovereign-cloud credentials | From €2/mo | Instance locations limited to Paris, Amsterdam and Warsaw |
| Contabo | The most RAM and disk per euro | €5.50/mo (4 vCPU, 8 GB, 100 GB) | 200 Mbit/s port at the entry tier |

A few niche options sit outside this table: AWS Lightsail ($5/month for 2 vCPU, 0.5 GB RAM, 20 GB storage, 1 TB transfer) makes sense for teams already inside AWS; IONOS is the German peer with enterprise SLAs, BSI C5 and IT-Grundschutz compliance; and Leaseweb covers dedicated hardware outside Hetzner's map, with featured servers including 30 TB of traffic from €60.13/month ex VAT across nine countries.

## Vultr in depth: the closest like-for-like swap

Vultr earns the top spot among Hetzner alternatives because it copies the parts of Hetzner people actually like — pick a plan, deploy in minutes, pay by the hour with a monthly cap, no minimum contract — and changes the part they can't fix: footprint. Vultr operates 33 regions across North America, Europe, Asia, Australia, South America and Africa, including locations Hetzner doesn't serve at all. It also sells things Hetzner's cloud line doesn't: NVIDIA GPU instances for AI workloads and Windows servers, where Hetzner's cloud product is Linux-only.

| Vultr plan | What you get | Price | Billing |  |
| --- | --- | --- | --- | --- |
| Cloud Compute — entry, IPv4 | 1 vCPU, 0.5 GB RAM, 10 GB storage, 0.5 TB transfer | $3.50/mo | Hourly, capped at the monthly rate | [See the entry plan](https://www.vultr.com/pricing/?ref=7268283) |
| Cloud Compute — entry, IPv6-only | Same entry class without an IPv4 address | $2.50/mo | Hourly, capped at the monthly rate | [See the IPv6-only plan](https://www.vultr.com/pricing/?ref=7268283) |
| High Frequency Compute | Alternate compute line on the same account | Varies by size | Hourly, capped | [Compare compute lines](https://bit.ly/VulTR) |
| Bare Metal | Single-tenant dedicated servers | Varies by configuration | Quoted per server | [See bare metal options](https://bit.ly/VulTR) |
| GPU | NVIDIA GPU instances for AI workloads | Varies by GPU type | Hourly | [Check GPU plans](https://bit.ly/VulTR) |

The billing model deserves a sentence of its own, because it's the thing Hetzner users notice first. Vultr bills hourly and caps the charge at the monthly price, so a test server you destroy after two days costs a fraction of the sticker rate — same as Hetzner's approach, and one of the reasons the swap feels familiar.

Now the catches. A production instance on Vultr usually costs more than the headline number: backups add roughly 20% of the instance cost, snapshots are billed per GB, and bandwidth above the included allowance is billed per GB too. If you switch on backups and keep snapshots around, budget for it. The second catch is transfer: the entry plan includes 0.5 TB, which is a fraction of Hetzner's EU allowance — more on that below. And at higher specs inside Hetzner's home regions, Hetzner usually keeps its price-to-performance lead, so "switch because it's cheaper" only holds at the entry tier.

If the region list and the plan structure make sense for you, 👉 [open Vultr's pricing page](https://www.vultr.com/pricing/?ref=7268283) and line its plans up against your current Hetzner invoice before deciding.

## Traffic: the detail that decides most Hetzner migrations

On paper, this is the biggest sacrifice you make by leaving. Hetzner's European servers include at least 20 TB of monthly traffic (US servers at least 1 TB, Singapore 0.5 TB). Vultr's entry plan includes 0.5 TB, DigitalOcean's cheapest 500 GB, Akamai's 1 TB — and Vultr charges per GB beyond the allowance.

So measure before you move. Pull last month's actual transfer numbers from your Hetzner panel. If you're moving under half a terabyte a month — true for most small sites and APIs, and equivalent to many millions of page requests — the entry allowances at Vultr, DigitalOcean or Akamai won't even register. If you run a CDN origin, backup target or media server through Hetzner's 20 TB, the math flips completely, and two alternatives handle traffic differently:

- **OVHcloud** bundles unmetered traffic into every VPS plan, with anti-DDoS protection and daily backups included. The limit moves to port speed instead: capped per plan from 500 Mbit/s on the entry VPS up to 3 Gbit/s on VPS-4.
- **Scaleway** takes the opposite approach — its list prices include egress, so there are no outbound transfer fees at all — but caps instance bandwidth per type, starting at 100 Mbps.

Contabo's cheap boxes come with their own built-in traffic limiter of a different kind: a 200 Mbit/s port at the entry tier. Fast pipes cost extra there.

## When a specialist beats the generalists

If you're chasing one specific thing, a specialist usually does it better than any all-rounder — and several of them are cheaper than Hetzner's post-increase prices.

**Contabo** is the RAM-and-disk answer. Cloud VPS 4 lists at €5.50/month with 4 vCPU, 8 GB of RAM and 100 GB of SSD — more memory than Hetzner's CPX22 at €19.49, for about a quarter of the new price. The trade is the port: 200 Mbit/s at entry, reaching 1 Gbit/s only at €37/month on Cloud VPS 16. Memory-hungry, low-traffic workloads are its natural home. One ownership note: Contabo has been US-private-equity-owned since 2022, though it still operates from the EU.

**netcup** is the German contract play: €8.26/month ex VAT for 2 vCores, 4 GB of RAM and 64 GB of storage on a 12-month term, with 1-, 12- and 24-month options and a footprint running from Vienna, Nuremberg and Amsterdam to a US location and Singapore. Committing to a term is how the price stays low — if you need month-to-month flexibility, look elsewhere.

**Scaleway** is the sovereignty pick. It's French, Iliad-owned, and holds ANSSI SecNumCloud qualification, which matters for French public-sector work; the catalogue runs from €0.43/month instances up through GPU, serverless, Kubernetes and even Apple silicon. No egress fees make it quietly interesting for traffic-heavy setups.

**UpCloud** covers the middle ground Hetzner vacated: €3/month for 1 vCPU, 1 GB RAM and 10 GB storage, hourly billing, and nine EU regions among 14+ data centers worldwide. Its hourly cap tops out at 28 days per month, so an always-on server bills as if it ran 28 days — a small permanent discount.

**DigitalOcean** is the tooling pick. The $4 entry Droplet is thin on RAM, but that's rarely why people choose it: managed PostgreSQL, MySQL and Kubernetes live in the same control panel, billing is per-second (since January 1, with a 60-second minimum and a 672-hour monthly cap), and the tutorial library is the deepest in the category. Its App Platform also ships a free tier — rare in this crowd.

## When staying with Hetzner is still the right call

If your users are in Europe or the eastern US and your stack runs on Linux, the case for leaving is weaker than the search results imply. Hetzner's price per core on dedicated hardware in Germany and Finland remains the European reference — nothing in the comparisons above beats it there — and its dedicated-server auction market is a price-hunting tool with no real equivalent elsewhere in Europe. The 20 TB EU traffic allowance and hourly billing with no contract both survived the price changes.

A hybrid is also worth naming: plenty of teams keep Hetzner for the EU footprint and run the rest of the world on Vultr. That split gets you the best of each map instead of forcing one provider to cover all of it.

## Moving off Hetzner without losing a weekend

The one technical trap: Hetzner snapshots can't be exported. The migration happens at the application and data layer, not the image layer.

So do it in this order. First, get your infrastructure into code — Terraform or Ansible — and verify it against Hetzner before porting the definitions; this turns an error-prone copy job into a re-deploy. Then move stateless workloads first and data last: deploy application servers on the new provider, point them at the databases still running on Hetzner, and test under real traffic before touching state. Both ends sit in EU data centers for most migrations, where latency typically runs 5–25 ms, so the temporary split is barely noticeable.

## Hetzner alternative questions, answered

**What's the cheapest Hetzner alternative?**
Vultr's $2.50 IPv6-only plan is the lowest flat entry price among the established clouds, with $3.50 adding IPv4. In Europe, Contabo's €5.50 box is the most hardware per euro if you don't need port speed, and Scaleway's instances start even lower.

**Is Vultr cheaper than Hetzner now?**
At the entry tier, yes on headline price: $3.50 with IPv4 included, versus Hetzner's increased cloud plans — the CX23, for instance, now lists at €5.49 before VAT and IPv4. At higher specs in Hetzner's home regions, Hetzner usually keeps the price-to-performance edge. And exchange rates move, so check the euro-dollar rate before declaring a winner.

**Do any Hetzner alternatives include a free tier?**
Rarely. Among the commonly listed options, DigitalOcean's App Platform and AWS Amplify ship free tiers; Hetzner and Vultr don't offer a permanent free compute tier — Vultr's floor is the $2.50–3.50 plans instead.

**Which alternative gives me unmetered bandwidth?**
OVHcloud (unlimited traffic, port speed capped per plan) and Scaleway (no egress fees, bandwidth capped per instance type). Both swap the traffic meter for a different limit, so check which limit hurts your workload less.

**Does Vultr support Windows or GPUs?**
Yes to both — Windows-licensed servers and NVIDIA GPU instances are available, while Hetzner's cloud line is Linux-only. Neither is priced at a single flat rate; cost depends on the plan. 👉 [See Vultr's plan options for Windows and GPU](https://bit.ly/VulTR)

## Picking by situation

One last pass through the decision, based on the numbers above:

- Users spread across several continents, or in South America, Africa or Asia → **Vultr**, for the 33-region map and the $3.50 floor.
- Traffic-heavy EU workload (CDN origins, backups, media) → stay on Hetzner for the 20 TB, or look at OVHcloud and Scaleway's egress-free pricing.
- Maximum RAM and disk per euro, modest traffic → **Contabo** (mind the 200 Mbit/s port) or **netcup** on a 12-month term.
- Managed databases and Kubernetes next to your VMs → **DigitalOcean**.
- French public-sector or SecNumCloud requirements → **Scaleway** or **OVHcloud**.
- German enterprise compliance (BSI C5, IT-Grundschutz) → **IONOS**.
- Dedicated hardware outside Hetzner's regions → **Leaseweb**.

If Vultr is the fit, start small: the entry plan is cheap enough to test a region properly before you commit anything bigger. 👉 [Open Vultr's pricing page, pick your region, and start with the $3.50 plan](https://www.vultr.com/pricing/?ref=7268283)
