# CoreSite LA2 VPS: Who Sells Inside the Building, What $20 a Month Buys, and Why the Residential IP Plans Can't Host a Website (Full Plan Table + Same-Building Price Check)

CoreSite LA2 at 900 N. Alameda Street in downtown Los Angeles hosts more than one VPS seller, and the plans inside it fall into two separate jobs: normal web and application hosting, or residential-IP work such as social accounts, SEO and marketplace operations. SixtyNet sells both from that building. Its LAX line starts at **$20/month** for 2 vCPU, 2GB RAM, 40GB NVMe and 5TB of traffic; its AT&T Mobility residential-IP line starts at **$15/month**, with one catch that decides everything: **ports 80 and 443 are closed on every residential plan**, so none of them can serve a normal website.

What follows is the full plan table, a price comparison against other sellers in the same building, the annual billing math per plan, and the three things that cost people money when they discover them after ordering.

> **Quick pick.** Running a site or an app: **LAX-MICRO at $40/month** (4 vCPU, 4GB, 80GB NVMe, 10TB traffic), or LAX-STARTER at $20/month if your traffic is small. Managing social or marketplace accounts: **Residential-MICRO at $35/month**, since 2GB of RAM runs thin once an anti-detect browser is open. 👉 [See SixtyNet's current LA2 plan pricing](https://sixtynet.net/aff.php?aff=39)

## SixtyNet's LA2 plans in full

Every plan below runs on KVM on AMD EPYC processors with DDR4 3200MHz memory and NVMe storage, managed through the VirtFusion panel (OS rebuild, reboot, VNC console, snapshots). The OS list covers CentOS, Debian, Ubuntu, Fedora, Arch, openSUSE, AlmaLinux, FreeBSD, OpenBSD, CoreOS and Windows, custom ISO upload is allowed, and there are 400+ one-click installers including cPanel, Plesk, CyberPanel, Webmin, Docker, WordPress, Joomla, Drupal, Magento and PrestaShop. The brand advertises DDoS mitigation above 1000Gbps, hardware CC-attack mitigation, free daily backups, free SSL and a **99.9% uptime** target.

Storage throughput is listed as 12,500 IOPS on the two smaller plans in each line and 25,000 IOPS on the 8-core and 16-core plans. Network port speed scales with the plan, from 2G on the smallest configurations to 10G on the top two.

These are the published plan figures; the checkout page is the number you actually pay.

### Standard LAX plans (ports 80/443 open)

| Plan | vCPU / RAM | NVMe | Traffic | Price | Order |
| --- | --- | --- | --- | --- | --- |
| LAX-STARTER | 2 / 2GB | 40GB | 5TB | $20/mo or $200/yr | [Order LAX-STARTER](https://sixtynet.net/aff.php?aff=39) |
| LAX-MICRO | 4 / 4GB | 80GB | 10TB | $40/mo or $400/yr | [Order LAX-MICRO](https://sixtynet.net/aff.php?aff=39) |
| LAX-MEDIUM | 8 / 8GB | 160GB | 20TB | $80/mo or $800/yr | [Order LAX-MEDIUM](https://sixtynet.net/aff.php?aff=39) |
| LAX-LARGE | 8 / 16GB | 320GB | 40TB | $160/mo or $1,600/yr | [Order LAX-LARGE](https://sixtynet.net/aff.php?aff=39) |

### Residential IP plans (AT&T Mobility addresses, **80/443 closed**)

| Plan | vCPU / RAM | NVMe | Traffic | Price | Order |
| --- | --- | --- | --- | --- | --- |
| Residential-STARTER | 2 / 2GB | 40GB | 5TB | $15/mo or $140/yr | [Order Residential-STARTER](https://sixtynet.net/aff.php?aff=39) |
| Residential-MICRO | 4 / 4GB | 80GB | 10TB | $35/mo or $340/yr | [Order Residential-MICRO](https://sixtynet.net/aff.php?aff=39) |
| Residential-MEDIUM | 8 / 8GB | 160GB | 20TB | $75/mo or $740/yr | [Order Residential-MEDIUM](https://sixtynet.net/aff.php?aff=39) |
| Residential-LARGE | 16 / 16GB | 320GB | 40TB | $155/mo or $1,540/yr | [Order Residential-LARGE](https://sixtynet.net/aff.php?aff=39) |

The residential line is the reason many people find this brand at all. The IPs come from AT&T Mobility rather than a datacenter block, which is what makes them useful for platform accounts that treat datacenter ranges as a signal. The trade is explicit in the plan page: because of IP risk control, **80 and 443 stay shut**, and the intended workloads are social media management, SEO, e-commerce operations, market research and scraping. If you want a public site, that is the LAX table, not this one.

### Storage plans (RAID 10)

| Plan | vCPU / RAM | Storage | Traffic | Price | Order |
| --- | --- | --- | --- | --- | --- |
| LAX-Storage-500G | 4 / 4GB | 500GB RAID 10 | 10TB | $40/mo or $400/yr | [Order LAX-Storage-500G](https://sixtynet.net/aff.php?aff=39) |
| LAX-Storage-1TB | 8 / 8GB | 1TB RAID 10 | 15TB | $70/mo or $700/yr | [Order LAX-Storage-1TB](https://sixtynet.net/aff.php?aff=39) |

RAID 10 means mirroring plus striping, so you keep redundancy and most of the speed. For media archives, backups of client sites or a self-hosted Nextcloud, the 500GB plan at $40 gives you more usable disk than LAX-MICRO at the same monthly price, at the cost of NVMe-level throughput on the storage volume.

## Why put a VPS in CoreSite LA2 at all

LA2 is a Tier III+ certified facility at 900 N. Alameda Street, Los Angeles, CA 90012, with N+1 redundant power backed by UPS and generators, redundant HVAC, 24/7 on-site security with biometric access control and CCTV. The building sits on high-count dark fiber and offers direct connections to AWS, Azure and Google Cloud, plus extensive peering at the major US exchanges. CoreSite positions it for US West presence, media workloads and latency-sensitive US-APAC paths.

For a VPS buyer, that translates into three practical things: your traffic enters a dense peering ecosystem instead of a single transit pipe, cloud on-ramps to the three big providers are physically nearby if you split workloads, and the power and cooling are certified rather than claimed.

SixtyNet's own pitch for the location is Any2 peering plus China-optimized routing for Asia-bound traffic. The plan page lists China Unicom Premium (AS9929) among its network options. It does not publish latency figures or a full transit list, so treat the China optimization as a brand claim to verify with your own test rather than a spec you can budget against. 👉 [Check the LA2 network options and plan availability](https://sixtynet.net/aff.php?aff=39)

## Same building, same $20: what your money buys

Two sellers in LA2 will take exactly $20 a month and hand you different machines. This is the comparison most LA2 write-ups skip.

| Provider (LA2) | Plan at ~$20 | vCPU / RAM | Disk | Traffic |
| --- | --- | --- | --- | --- |
| SixtyNet | LAX-STARTER $20/mo | 2 / 2GB | 40GB NVMe | 5TB |
| Misaka | S3N-2C4G $20/mo | 2 / 4GB | 64GB NVMe | 4TB |
| Servers Factory | Starter $25/mo | 2 / 2GB | 20GB | 2TB |

SixtyNet's $20 buys 1TB more traffic; Misaka's buys double the RAM and 60% more disk. If you are running a memory-hungry app (Java, a busy MySQL instance, a container stack), the extra 2GB matters more than the extra terabyte, which most small sites never touch. If you are serving lots of static assets or proxying video, the 5TB is the better trade.

Misaka's range also starts lower: its 1 vCPU / 1GB / 16GB / 1TB plan is $6/month, and it publishes its transit list including China Telecom CN2 (AS4809), China Unicom Global (AS10099) and China Mobile International CMIN2 (AS58807) as named routes. If knowing the exact Chinese carrier path before you pay is a requirement, that transparency is worth something. SixtyNet's advantage is the combination: a $15 entry point and residential IPs available from the same account, which almost no LA2 competitor offers.

Two other names in the building, Servers Factory and RackCorp, run colocation and cloud/virtual servers on Cisco Nexus 10G switching and CEPH-based storage; RackCorp does not publish VPS pricing, and Servers Factory's plan page carries testimonials dated 2020, so treat its numbers as reference rather than a live quote. None of them sell residential IPs.

## Three things that catch buyers out

**1. The residential plans cannot serve a website.** Ports 80 and 443 are closed by design on all four residential tiers. Nothing you configure on the server changes that. If your plan is "cheap VPS with a residential IP, and I'll also park my store on it," the store will not load. Pick a LAX plan for anything that answers HTTP, and keep residential for outbound work: account management, scraping, ad verification, local-market research.

**2. The refund window is 3 days, not 30.** Three days is enough to run a disk benchmark, install your stack and check whether the route to your users is acceptable. It is not enough to wait for a support ticket to be resolved before you decide. Book the test window before you order, and pay monthly on the first cycle rather than annual, so a bad fit costs you one month instead of a year.

**3. Credit card payments are listed as suspended** as an anti-fraud measure, with other methods required at checkout. Confirm what your method costs before you commit, since third-party processors can add fees of their own. 👉 [Start with a monthly plan and use the 3-day refund window to test](https://sixtynet.net/aff.php?aff=39)

## The annual math, plan by plan

SixtyNet's page advertises annual billing as roughly 17% off. Per plan, the real numbers are these:

| Monthly | Monthly × 12 | Annual | You save |
| --- | --- | --- | --- |
| LAX-STARTER $20 | $240 | $200 | $40 (16.7%) |
| LAX-MICRO $40 | $480 | $400 | $80 (16.7%) |
| LAX-MEDIUM $80 | $960 | $800 | $160 (16.7%) |
| LAX-LARGE $160 | $1,920 | $1,600 | $320 (16.7%) |
| Residential-STARTER $15 | $180 | $140 | $40 (22.2%) |
| Residential-MICRO $35 | $420 | $340 | $80 (19.0%) |
| Residential-MEDIUM $75 | $900 | $740 | $160 (17.8%) |
| Residential-LARGE $155 | $1,860 | $1,540 | $320 (17.2%) |

Two things worth noting. The absolute saving is identical at each tier across both lines ($40, $80, $160, $320), so the discount percentage is highest on the cheapest residential plan and flattens as you scale. And the residential discount (17–22%) is larger than the LAX discount (16.7%), which is the opposite of what the generic "17% off annual" line implies. Do your arithmetic on the plan you are actually buying.

Renewal pricing is not published on the plan page, so the year-two cost is a question for the checkout page or support before you commit to an annual term. Nobody can tell you it stays flat, including this article.

## Which plan fits which job

**A blog, a brochure site or a small WordPress install:** LAX-STARTER at $20. Two cores and 2GB handle a cached WordPress site comfortably. Add a CDN before you add RAM.

**WooCommerce, a membership site or several client sites on one box:** LAX-MICRO at $40. The jump to 4GB is the one upgrade that reliably prevents the database from being the bottleneck.

**Development and staging:** LAX-STARTER on monthly billing. Snapshots and custom ISO upload mean you can break and rebuild the box without a support ticket, and monthly billing keeps you free of a year-long commitment while you decide.

**Social accounts, SEO tools, price scraping, ad verification:** Residential-MICRO at $35. The 2GB STARTER runs out once you open a few browser profiles, and the four cores make parallel sessions usable.

**Media archives, backups, self-hosted file sync:** LAX-Storage-500G at $40. More usable disk per dollar than any NVMe plan in the lineup.

**What most people don't need:** LAX-LARGE at $160 and Residential-LARGE at $155. Both exist to move 20–40TB of traffic with 16GB of RAM. If your monthly transfer is under 5TB, which covers the large majority of sites and account-management setups, you are paying for headroom you will never use. Step up from MICRO to MEDIUM only when you can point at the resource that is actually maxing out.

## FAQ

**Where is CoreSite LA2, and does the location actually matter?**
900 N. Alameda Street, downtown Los Angeles. It matters for two reasons: dense peering and cloud on-ramps to AWS, Azure and Google Cloud inside the same building, and a west-coast position that shortens the transpacific path compared with east-coast facilities.

**Can I host a website on a residential IP plan?**
No. Ports 80 and 443 are closed on all four residential plans because of IP risk control. Use the LAX line for anything that serves HTTP.

**Is 3 days enough to evaluate the service?**
For performance, yes: run a disk benchmark, install your stack, test the route from your users' locations, all within the first day. For support quality, no, because a complex ticket may take longer than the window. Test what you can control, and start monthly.

**Can I install Windows or upload my own ISO?**
Yes. The OS template list includes Windows, FreeBSD, OpenBSD and the main Linux distributions, custom ISO upload is supported, and the VirtFusion panel lets you rebuild, reboot, open a VNC console and roll back a snapshot yourself.

**Will it be fast from mainland China?**
The brand states China-optimized routing and lists China Unicom Premium (AS9929) among its network options, but publishes no latency data and no complete transit list. Test it during the refund window from the networks your users are on instead of relying on the claim.

## How to decide

Match the plan to the job and ignore the rest of the lineup. Serving web traffic: LAX-STARTER at $20 if you are small, LAX-MICRO at $40 if a database is involved. Residential IP work: Residential-MICRO at $35. Bulk storage: LAX-Storage-500G at $40. Everything above that is for people moving tens of terabytes.

Before you pay, confirm two things on the checkout page: which payment methods are live while cards are suspended, and what your plan renews at, since renewal pricing is not published. Then use the 3-day window properly rather than treating it as a formality. 👉 [Compare SixtyNet's LA2 plans and pick your configuration](https://sixtynet.net/aff.php?aff=39)
