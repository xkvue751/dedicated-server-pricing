# Dedicated Server Pricing: Real Monthly Costs From Bare Metal to Dedicated vCPUs, and the Promo-Reset Math Most Providers Skip

Renting an entire physical server costs anywhere from €5.99 to well over €700 a month, and both ends of that range are real, published prices: Kimsufi's entry line sits at €5.99 excl. VAT, while a dual-socket EPYC storage server at DediCrypto runs $745/mo. The band most people actually shop in — an entry dedicated box that can hold a production workload — runs roughly $40 to $130 a month across Namecheap, Hivelocity, DediCrypto, and Vultr.

Headline prices in this market come with two fine-print problems, and neither shows up in the pricing table you'll screenshot. First-year promos reset: Namecheap's $41.53/mo entry config renews at $69.88, and Hivelocity's $97/mo promo config renews at $129. Add-ons quietly stack too: Kimsufi tracked twelve of its own configurations for six months and found the real monthly cost ran 22% above the headline once setup fees, backup storage, and licenses were included.

So this guide does three things: lays out verified dedicated server pricing across the vendors people actually compare, runs the two-year math on those promo resets, and covers the option most price-comparison articles skip — dedicated vCPUs, which start at $28/mo on Vultr and solve the problem half of dedicated-server shoppers are really trying to fix.

> **Quick verdict**
>
> - **Need guaranteed CPU with no lock-in:** Vultr's Optimized Cloud Compute starts at **$28/mo**, billed hourly, cancellable anytime.
> - **Need an actual single-tenant machine:** Vultr bare metal starts at **$120/mo** with no setup fee.
> - **Want the cheapest fixed monthly bill and can run your own ops:** Namecheap's entry Xeon at $41.53/mo (first year) or Hivelocity's $97/mo promo config — both renew higher; the math is below.
>
> 👉 [Check Vultr's current plans and hourly rates](https://www.vultr.com/pricing/?ref=7268283)

## How much does a dedicated server actually cost right now?

Verified list prices currently run from €5.99 to $745 per month. Here's the entry offer from each vendor worth comparing, including the renewal behavior that the headline price hides. All figures were checked against each vendor's published pricing pages between July and September 2026.

| Provider | Entry config | Headline price | What happens at renewal |
| --- | --- | --- | --- |
| Kimsufi (OVHcloud) | 4-core Intel/AMD, 16–64 GB RAM | €5.99/mo excl. VAT | Flat list price; typical add-ons (extra IP, 50 GB backup, control panel) push it to ~€8.50/mo |
| Namecheap | Xeon E-2234, 4C/8T, 16 GB ECC, 480 GB SSD | $41.53/mo first year | Renews at $69.88/mo — the "41% off" applies to year one only |
| Hivelocity | Xeon E-2236, 16 GB | $97/mo promo | Renews at $129/mo regular rate |
| DediCrypto | Ryzen 9 7950X, 16C/32T, 128 GB DDR5 | $110/mo | Flat; −3% quarterly, −8% annual; crypto-only checkout |
| Vultr (bare metal) | 4-core Xeon E3-1270v6, 32 GB ECC, 2×240 GB SSD | $120/mo | Flat list price, no setup fee |
| Liquid Web (managed) | 16-core Xeon, 64 GB | $167.50/mo | Flat; includes full management, migration included |

Three things the table can't show. First, this market's floor rotates constantly — Hivelocity's flat $75/mo config that reviewers recommended in August had left inventory by September, so treat any specific bargain config as perishable. Second, "entry level" means wildly different hardware at different vendors: Namecheap's cheapest is a 4-core Xeon E-2234 with a single SATA SSD, while DediCrypto's entry is a current-gen Ryzen 9 7950X with 128 GB of DDR5 and 2×1.92 TB NVMe. Compare the CPU generation, memory, and disk before the price. Third, managed support changes the product entirely — Liquid Web's $167.50 floor buys operations staff, and in this case more hardware than the unmanaged entries too.

## Vultr's compute plans at a glance

Vultr sells the full spectrum, from $5/mo shared cloud instances up to single-tenant bare metal at $120/mo, with no setup fees and data centers in 30-plus regions. The question that actually matters for this article is which of its four compute families matches what you're shopping for:

| Plan family | Entry configuration | Price from | Billing | Best for | Order |
| --- | --- | --- | --- | --- | --- |
| Cloud Compute — Regular Performance (shared CPU) | 1 vCPU, 1 GB RAM, 25 GB SSD, 1 TB transfer | $5/mo | Hourly, capped at monthly rate | Dev boxes, small sites | [ Deploy cloud compute](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| Cloud Compute — High Performance (shared CPU, NVMe) | 1 vCPU, 1 GB RAM, 25 GB NVMe, 2 TB transfer | $6/mo | Hourly, capped at monthly rate | Production sites that need faster storage | [ Deploy high performance](https://www.vultr.com/products/cloud-compute/?ref=7268283) |
| Optimized Cloud Compute (dedicated vCPUs) | 1 dedicated vCPU, 4 GB RAM, 25 GB NVMe, 2 TB transfer | $28/mo | Hourly, capped at monthly rate | CPU-bound apps, game servers, CI runners | [ View dedicated vCPU plans](https://www.vultr.com/products/optimized-cloud-compute/?ref=7268283) |
| Bare Metal | Xeon E3-1270v6, 4C/8T, 32 GB ECC, 2×240 GB SSD, 1 Gbps | $120/mo | Monthly | True single-tenant workloads | [ Deploy bare metal](https://www.vultr.com/products/bare-metal/?ref=7268283) |

(Vultr also sells storage, networking, managed databases, and Kubernetes products that price separately; for dedicated-server shoppers, the four compute families above are the decision.)

Because the Optimized Cloud Compute line is the one most people comparing dedicated prices should scrutinize, here's its full step ladder — every tier doubles the cores:

| Dedicated vCPUs | RAM | NVMe storage | Transfer | Monthly | Deploy |
| --- | --- | --- | --- | --- | --- |
| 1 | 4 GB | 25 GB | 2 TB | $28 | [ Start at 1 vCPU](https://www.vultr.com/products/optimized-cloud-compute/?ref=7268283) |
| 2 | 8 GB | 50 GB | 3 TB | $56 | [ Deploy 2 vCPUs](https://www.vultr.com/products/optimized-cloud-compute/?ref=7268283) |
| 4 | 16 GB | 100 GB | 4 TB | $112 | [ Deploy 4 vCPUs](https://www.vultr.com/products/optimized-cloud-compute/?ref=7268283) |
| 8 | 32 GB | 200 GB | 5 TB | $224 | [ Deploy 8 vCPUs](https://www.vultr.com/products/optimized-cloud-compute/?ref=7268283) |
| 12 | 48 GB | 300 GB | 6 TB | $336 | [ Deploy 12 vCPUs](https://www.vultr.com/products/optimized-cloud-compute/?ref=7268283) |
| 16 | 64 GB | 400 GB | 8 TB | $448 | [ Deploy 16 vCPUs](https://www.vultr.com/products/optimized-cloud-compute/?ref=7268283) |

Optimized Cloud Compute also comes in General Purpose, Memory Optimized, and Storage Optimized classes when you need more RAM or disk per core than the pure vCPU line offers.

## Why the second year matters more than the first

Promo pricing is the standard playbook at the cheap end of this market, and the renewals are steep enough to change the ranking. Namecheap's 41%-off first year turns $41.53 into $69.88 on renewal — a 68% jump. Over two years, that entry config costs $1,336.92, which works out to an effective $55.70/mo. Hivelocity's $97 promo renews at $129, giving a two-year effective of $113/mo. DediCrypto and Vultr publish flat rates: DediCrypto takes 3% off quarterly billing and 8% off annual, and 👉 [Vultr's bare metal rate is the same in month 25 as in month 1](https://www.vultr.com/products/bare-metal/?ref=7268283).

One honest wrinkle here. On pure two-year math, Hivelocity's effective $113/mo slightly undercuts Vultr's flat $120 bare metal. If you're committed to a fixed Linux box for two-plus years and handle your own patching, firewalling, and backups, Hivelocity's numbers hold up — it also runs 40-plus data center locations and provisions hardware fast. Vultr's counter-argument is flexibility: hourly billing on its cloud instances, no contracts, and the same account can scale from a $5 instance to bare metal as your needs change. There's also the inventory problem — vendors at this price tier reshuffle configs without much warning, as Hivelocity's vanished $75 box demonstrated.

## Bare metal or dedicated vCPUs? Most buyers pick the wrong one

A lot of people searching for dedicated server pricing are chasing one of two things: guaranteed CPU that nobody else can steal, or a machine nobody else can touch. Bare metal delivers both. Dedicated vCPUs deliver the first at roughly a quarter of the price.

Pick bare metal when you genuinely need it. Some software licenses charge per physical socket, some compliance frameworks want single-tenant hardware, and virtualization-heavy projects — your own hypervisor hosts, custom kernel work, high-throughput storage — want the real machine. In those cases, the ~$97–$120 entry band is the honest price of admission, and no shared product substitutes for it.

Pick dedicated vCPUs when the complaint is performance variance. Vultr's Optimized Cloud Compute pins cores to your instance — no noisy neighbors — on NVMe storage, starting at $28/mo for one reserved core. If your story is "my app gets slow at peak," that's usually the fix, and it costs a lot less than a whole server.

The billing model is the second reason to look here. Vultr meters cloud instances by the hour and caps the bill at the monthly rate, so cost tracks usage. A 1-vCPU dedicated box used 12 hours a day on weekdays burns about 264 hours a month — call it $11 on the hourly meter instead of $28 flat. Traditional dedicated vendors can't price that way; you'd pay the full month for a machine that sits idle every night and weekend. For bursty workloads, that gap is the entire decision. 👉 [See Vultr's dedicated vCPU plans and hourly rates](https://www.vultr.com/products/optimized-cloud-compute/?ref=7268283)

## The add-on costs that pad the final bill

Whatever sticker price you land on, expect the final bill to run 15–30% higher once add-ons are counted. Kimsufi's own guide puts the typical uplift in that range, and its six-month tracking measured the average at 22%. Its worked example: the €5.99 entry server becomes roughly €8.50/mo with an extra IP, 50 GB of backup storage, and a control panel license.

The usual suspects:

- **Backups.** Vultr's automatic backups cost 20% of the instance's price, added to the monthly bill. Cheap but real.
- **Setup fees.** Vultr and DediCrypto charge $0. Some legacy dedicated vendors still charge setup on certain SKUs, and it tends to surface only at checkout.
- **Bandwidth overages.** DediCrypto includes unmetered 1 Gbps on every config; Vultr bills per gigabyte past your plan's transfer allowance instead of throttling the port. A steady 20 TB/month streamer and a bursty blog get punished by opposite pricing structures — match the model to your traffic before comparing monthly fees.
- **Management.** The unmanaged discount is effectively a payment for your own time. Patching, monitoring, incident response at 3 a.m. — that's what separates a $97 Hivelocity box from Liquid Web's $167.50 managed floor, and it's also why Liquid Web includes migration while Hivelocity sells it as an add-on.
- **Licensing.** Windows, SQL Server, and control panels sit on top of the base price at every vendor on this page.

## Dedicated server pricing FAQ

**How much does a dedicated server cost per month?**

Between roughly €5.99 and $745 as of the latest checks, with the practical entry band at $40–130/mo for usable single-tenant hardware. Managed dedicated hosting starts around $167.50/mo at Liquid Web.

**Do "from" prices renew at the same rate?**

Often no. Namecheap's entry config jumps from $41.53 to $69.88 after year one, and Hivelocity's $97 promo resets to $129. Budget on the renewal figure, and treat the discount as a bonus rather than the reason you're buying.

**Is a dedicated server still worth it over a VPS?**

For steady, pinned workloads — databases, game servers, steady-traffic production apps — yes, because you get predictable performance and per-core economics. For bursty traffic, an hourly-billed cloud instance usually costs less in practice than an always-on dedicated box sized for peak.

**What's the difference between bare metal and a dedicated vCPU?**

Bare metal is an entire physical machine reserved for you — kernel-level control, no virtualization layer, full hardware. A dedicated vCPU is a reserved core inside a shared physical host: you keep the no-neighbor performance guarantee but lose direct hardware access. Most "my server is slow" problems are solved by the second one.

## Which one should you pay for?

Match the plan to the workload:

- **Bursty or growing app, want to resize or delete anytime:** Vultr's dedicated vCPU line at $28/mo, billed hourly.
- **Steady 24/7 load that wants real hardware without renewal games:** Vultr bare metal at a flat $120/mo.
- **A fixed Linux box for two-plus years at the lowest effective price, with your own ops skills:** Hivelocity works out to $113/mo effective over two years — just budget on the $129 renewal and re-check the catalog before ordering, since its cheap configs rotate.
- **You want someone else to answer the phone:** Liquid Web's managed floor at $167.50/mo.
- **Crypto checkout, unmetered gigabit, current-gen Ryzen or EPYC:** DediCrypto from $110/mo.

Two checks before you order any of them: confirm the renewal price rather than the promo badge, and price out your add-ons — backups, extra IPs, licenses — so month two doesn't surprise you. Then 👉 [compare Vultr's plans and current prices side by side](https://www.vultr.com/pricing/?ref=7268283) and pick the row that matches your workload instead of the biggest discount.
