# wordpress vps hosting：Which Plan Fits Your Site, What Renewals Really Cost, and the Refund Rules to Check Before You Pay

Most people searching for wordpress vps hosting want one thing: a server that runs WordPress without the monthly bill eating the project's budget. The short answer from this research: RackNerd's annual KVM specials start at **$21.99/year** (about $1.83/month) for 1 GB RAM, and the 2 GB plan at **$35.99/year** is the more realistic starting point for a real WordPress site. Renewal stays at the same price for as long you keep the service — the company states this explicitly in its FAQ, which is rare in the budget VPS space.

There are two catches you'll want to know before clicking buy, and most ranking articles barely mention either: the VPS is fully unmanaged (you install and maintain WordPress yourself), and RackNerd does not offer refunds by default once payment goes through. Both are manageable if you plan for them. This article walks through every currently listed plan, the actual cost math, and the cancellation rules worth checking first.

> **Quick picks**
> - Personal blog, a few hundred visits a day → 1 GB special, $21.99/year
> - Most WordPress sites, small business sites, a couple of installs → 2 GB special, $35.99/year (marked "Most popular" on the official specials page)
> - WooCommerce or a busier multi-site setup → 4 GB special, $59.99/year
>
> 👉 [See the 2 GB special at $35.99/year](https://my.racknerd.com/aff.php?aff=11397&pid=953)

## The Full RackNerd Annual Lineup for WordPress

RackNerd currently lists five annual KVM VPS specials, and all five can run WordPress. Every plan ships with full root access, 1Gbps port, RAID-10 SSD storage, one IPv4 address, KVM virtualization, and deployment in any of about 20 datacenter locations. Delivery is near-instant after payment, and the control panel (called ctrl) handles reboots, OS reinstalls, an HTML5 VNC console, and one-click app installs.

| Plan | vCPU / RAM | SSD | Monthly transfer | Price (annual) | Order |
| --- | --- | --- | --- | --- | --- |
| 1 GB KVM VPS | 1 / 1 GB | 20 GB | 3 TB | $21.99/yr | [ Get the 1 GB plan](https://my.racknerd.com/aff.php?aff=11397&pid=952) |
| 2 GB KVM VPS | 2 / 2 GB | 35 GB | 5 TB | $35.99/yr | [ Get the 2 GB plan](https://my.racknerd.com/aff.php?aff=11397&pid=953) |
| 4 GB KVM VPS | 3 / 4 GB | 60 GB | 7 TB | $59.99/yr | [ Get the 4 GB plan](https://my.racknerd.com/aff.php?aff=11397&pid=954) |
| 6 GB KVM VPS | 6 / 6 GB | 100 GB | 12 TB | $89.99/yr | [ Get the 6 GB plan](https://my.racknerd.com/aff.php?aff=11397&pid=955) |
| 8 GB KVM VPS | 7 / 8 GB | 150 GB | 20 TB | $119.99/yr | [ Get the 8 GB plan](https://my.racknerd.com/aff.php?aff=11397&pid=956) |

The renewal question is the one that matters most with cheap annual VPS deals, so here is the exact policy language from RackNerd's own specials page: "These RackNerd VPS specials are lifetime recurring. You can renew at the same rate for as long as you decide to keep the service." Over three years, the 2 GB plan costs $107.97 total. Many budget hosts charge double or triple that on renewal after year one.

Operating system choices at order time include Ubuntu, Debian, AlmaLinux, Rocky Linux, CentOS, and Fedora; custom ISO installs are available on request through a support ticket. For WordPress, Ubuntu 22.04 or 24.04 LTS is the practical choice — the most documentation, the fewest surprises.

## Annual Specials vs. the Monthly Lineup: The Real Cost Math

The annual specials get all the attention, but RackNerd also sells a standard KVM line billed mostly by the month. It's worth understanding both, because the price gap between them is enormous — roughly seven times per year for the same RAM tier.

| Plan | vCPU / RAM | SSD | Transfer | Price |
| --- | --- | --- | --- | --- |
| 512 MB | 1 / 512 MB | 30 GB | 500 GB | $26.99/year |
| 1 GB | 2 / 1 GB | 50 GB | 1 TB | $17.99/mo |
| 2 GB | 3 / 2 GB | 75 GB | 2 TB | $20.59/mo |
| 4 GB | 4 / 4 GB | 130 GB | 3 TB | $24.59/mo |
| 6 GB | 5 / 6 GB | 170 GB | 4 TB | $27.59/mo |
| 8 GB | 6 / 8 GB | 220 GB | 5 TB | $36.59/mo |
| 12 GB | 7 / 12 GB | 300 GB | 6 TB | $55.99/mo |

Two things in this table trip people up.

First, the counterintuitive one: the 512 MB standard plan costs **$26.99/year — more than the 1 GB special at $21.99/year**. Less RAM, more money. It's the only standard plan billed annually, and it only makes sense as a tiny utility box. If your goal is WordPress, the 1 GB special simply dominates it on both price and spec.

Second, the monthly plans exist for flexibility, not savings. The 2 GB monthly plan runs $20.59/month, or $247.08/year, versus $35.99/year for the 2 GB special. That's a 6.8x difference. What you're buying with monthly billing is the ability to walk away any month — which, given the refund situation described below, is exactly why the monthly line matters.

👉 [Start with a monthly plan to test the waters before committing to a year](https://bit.ly/RacKnerd)

## What "Unmanaged" Means for Your WordPress Site

RackNerd manages the hardware, the network, and the virtualization platform. Everything above that layer — installing WordPress, the web server, PHP, the database, caching, SSL certificates, security hardening, and backups — is yours. If you're comfortable following a tutorial or using a control panel, this is a feature: you pick the stack, and nothing on the server is fighting you.

The practical setup path for most people looks like this:

1. Order the VPS, choosing Ubuntu 22.04/24.04 LTS and your datacenter.
2. Install a management panel — BT Panel (aaPanel for English users) gives you a graphical interface with one-click WordPress deployment; WordOps or CyberPanel are better if you want Nginx with FastCGI caching and Redis without hand-configuring anything.
3. Point your domain's DNS at the VPS IP.
4. Put Cloudflare's free tier in front of the site. It adds caching, basic attack filtering, and hides your origin IP — near-zero cost for a meaningful performance and security bump.

On datacenter choice: RackNerd runs roughly 20 locations, including Los Angeles, San Jose, Seattle, New York, Chicago, Dallas, Ashburn, Atlanta, Tampa, Toronto, Amsterdam, London, Dublin, and Strasbourg. Pick whichever is closest to your readers — European audiences get a meaningfully faster site from Amsterdam or London than from a US East Coast box. One known limitation for readers with mainland China traffic: RackNerd doesn't offer CN2 GIA-style optimized routes. Los Angeles DC-02 (their Asia-optimized location) plus Cloudflare is the standard workaround; if China latency is your top priority, a provider selling CN2 GIA lines starting around $49.99/year will serve that use case better.

Who this setup doesn't suit: anyone who wants someone else to handle updates, backups, and breakage. Managed WordPress hosting typically runs $2.99–$11.99/month for comparable single-site use, and if you never want to see a terminal, that price buys real value. The VPS route wins on cost and control — a 2 GB dedicated-RAM KVM box at $3/month has no shared-hosting neighbor problem — but the maintenance is genuinely yours.

## The Refund and Cancellation Rules Most Reviews Skip

This is the part cheap-VPS roundups tend to gloss over, and it directly affects how you should buy. RackNerd's terms of service (last revised July 7, 2026) are blunt: **no refunds by default once payment is received**. Refund requests are reviewed case-by-case, with the reasoning being that provisioning already incurred real costs. There is no 7-day or 30-day money-back window.

The specific rules worth knowing:

- **Prepaid account credit is non-refundable** and can only be applied to other services, not withdrawn.
- **Immediate cancellation** terminates the VPS within about 24 hours and wipes all data, permanently. If you click it by accident, open a billing ticket right away — support can reactivate if you're quick.
- **To avoid auto-renewal**, submit a cancellation request through the client area at least 5 days before the renewal date (7 days for contract services, which mostly means dedicated servers). Miss the window and the charge stands, per the no-refund default.
- **Chargebacks trigger a $125–$250 administrative fee** and possible account suspension. Never dispute with your bank before trying a ticket.
- **Data survives nothing.** Whether you cancel, lapse on payment (most services auto-terminate 7 days after the due date), or get suspended, termination means permanent deletion with no recovery path. RackNerd states it is not responsible for data integrity in any circumstance — backups are 100% your job.

None of this is a reason to avoid RackNerd; it's the trade that makes $21.99/year economically possible. But it changes the smart buying strategy:

1. **Use the Looking Glass and test files first.** Every datacenter has public test IPs and downloadable test files, so you can check latency and throughput from your location before spending anything.
2. **Consider one month on the monthly line** as your trial. The 1 GB monthly plan at $17.99 costs less than a dollar a day and you can cancel anytime.
3. **Don't migrate your production database on day one** of an annual plan. Get the stack working and benchmarks looking right before the site depends on it.
4. If something is genuinely broken right after provisioning — VPS won't boot, IP unreachable — open a billing ticket immediately with logs and screenshots. That's the scenario where case-by-case refunds are actually granted.

On support quality more generally: reviews on Trustpilot and LowEndTalk describe tickets resolved within hours, including a user reporting a technical answer in about three hours. Support covers platform issues 24/7; application-level WordPress problems are still yours to fix.

## How RackNerd Compares on Price

A quick, link-free reality check against the alternatives people usually cross-shop:

- **Managed WordPress hosting** ($2.99–$11.99/month typical entry): hands-off, but shared resources and a much higher floor. A year of the cheapest tiers costs more than three years of RackNerd's 1 GB special.
- **Hourly-billed cloud VPS providers** (Vultr's cheapest regular tier runs $2.50/month for 1 vCPU/0.5 GB): maximum flexibility, no commitment, but $30/year for half the RAM of RackNerd's $21.99 special, and pricing that can change between renewal cycles.
- **CN2 GIA route specialists** (BandwagonHost, from about $49.99/year): the better pick specifically for mainland China latency, at roughly 2.3x the price of the equivalent RackNerd plan.

RackNerd's edge is the combination of KVM isolation, dedicated resources, a full gigabit port on every plan, and locked renewal pricing. Its gaps are the ones already covered: no managed support, no China-optimized routes, no default refund window.

## FAQ

**Will my renewal price go up?** No. The annual specials are lifetime recurring — the rate you order at is the rate you renew at, indefinitely, per the official FAQ.

**Can I host multiple WordPress sites on one plan?** Yes, there's no license limit — your ceiling is RAM, CPU, and disk. Two or three lightweight blogs fit fine on the 2 GB plan with caching; anything with WooCommerce or heavy plugins deserves the 4 GB.

**Which plan for a WooCommerce store?** 4 GB minimum. Every cart and checkout operation hits the database, and running out of PHP memory mid-checkout costs you real orders. The 4 GB special at $59.99/year is the sensible floor.

**What payment methods work?** Credit card and PayPal, plus Bitcoin and Alipay per third-party documentation. Note that PayPal and card payments give you an external dispute mechanism, while crypto and Alipay leave only the internal ticket system if something goes wrong.

**Is the 1 GB plan enough for WordPress?** For a blog doing a few hundred to a couple thousand visits a day with a caching plugin and a lightweight theme, yes. The honest caveat: 1 GB runs WordPress, but it doesn't run it comfortably once you add plugins, cron jobs, or traffic spikes. The 2 GB special exists for exactly that reason and costs $14 more per year.

## Before You Order

Match the plan to the site, not to the price tag:

- Just launching a personal blog → 1 GB special at $21.99/year
- A real site with plugins, a business presence, or two or three installs → 2 GB special at $35.99/year
- WooCommerce or moderate-to-heavy traffic → 4 GB special at $59.99/year
- Completely allergic to the command line → reconsider and look at managed hosting instead; it costs more and does the maintenance for you
- Mainland China latency is the deciding factor → a CN2 GIA specialist fits better, regardless of price

And before paying for a year of anything: run the Looking Glass test from your location, pick the datacenter nearest your readers, and set a calendar reminder for 7 days before next year's renewal date if you ever want out. That last step costs nothing and is the difference between a locked-in renewal charge and a clean exit.

👉 [Pick your datacenter and get your WordPress VPS running](https://bit.ly/RacKnerd)
