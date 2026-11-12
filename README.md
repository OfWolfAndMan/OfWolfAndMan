# OfWolfAndMan

*"I will either find a way, or I will make one."*

I'm a network engineer who builds infrastructure to be **extensible, modular, simple, and robust**, shaped by enough 2 AM maintenance windows to know what happens when documentation and production drift apart. Real networks are rarely single-vendor or tidy: Cisco, Arista, Juniper, Fortinet, and Linux regularly show up in the same week, each with its own CLI dialect and its own ways of failing.

## How I approach it

- **Automation is a system, not a pile of scripts.** Repeatable patterns across an estate beat one-off snowflakes and leave room for creativity on the edge cases that genuinely are odd.
- **Data quality comes first.** Automating on messy or unvalidated data just spreads failure faster. I anchor automation in a network source of truth, usually **Nautobot** paired with **Ansible** and **Python**, backed by schema validation.
- **Intent lives once, as data.** Subnets, VLANs, BGP peers, and security boundaries are defined in vendor-agnostic terms; platform-specific layers translate that intent for each device.
- **Check before changing.** Compare what a device has with what it should have before touching production. *"Is it already right?"* is the question that matters on the second run.
- **Say what has been tested.** If something has not run against real or virtual gear yet, the documentation says so up front.
- **Leave a clean trail.** Trade-offs, retirements, and breaking changes get written down for the next engineer, often me. What I publish now is scrubbed of credentials and private infrastructure details.

## Public work

Everything published here is deliberately narrower than my day-to-day production work.

**[Automate teh Network](https://github.com/OfWolfAndMan/Automate-teh-Network)** is where I work these ideas through publicly. Started in 2017 as Python 2.7 playbooks pushing full configurations, it now implements intent-based Ansible across Cisco IOS/IOS-XE, NX-OS, Arista EOS, and Linux. Playbooks are built on resource modules so a second run reports whether a device already matches intent, while compliance policies live as validated data that can be checked offline against saved configurations. Every playbook is labeled `verified`, `partial`, or `unverified`, CI runs an automated scrub to keep credentials and real addresses out, and a ground-up tutorial covers the fundamentals for anyone new to Ansible.

Other repositories:

- **[EVE-NG_Pipeline](https://github.com/OfWolfAndMan/EVE-NG_Pipeline)** — Jenkins and the EVE-NG API wired together to build and tear down full lab topologies on demand.
- **[CCIE-Lab-Automation](https://github.com/OfWolfAndMan/CCIE-Lab-Automation)** — Baseline provisioning, configuration backups, and operational diagnostics on IOSv and CSR1000V labs.
- **[chsheets](https://github.com/OfWolfAndMan/chsheets)** — A working field notebook of hardening notes, scripting references and red/blue team scripts.

*Archived:* Two earlier course repositories, [Network-Automation-Mini-Course](https://github.com/OfWolfAndMan/Network-Automation-Mini-Course) and [NotLayer3-NetworkAutomation](https://github.com/OfWolfAndMan/NotLayer3-NetworkAutomation), are retired. Everything worth keeping moved into Automate teh Network, and every retired file has either a successor or a written reason.

## Toolbox

- **Source of truth:** Nautobot (data modeling, Golden Config, GraphQL and REST APIs, Git-backed inventory) · schema validation
- **Network OS:** Cisco IOS, IOS-XE, IOS-XR, NX-OS · Arista EOS · Juniper Junos · Fortinet FortiOS · Linux routing and firewalling
- **Automation:** Ansible (resource modules, roles, Ansible Vault) · Python (Netmiko, NAPALM, ntc-templates, Jinja2, Flask, pytest, ruff)
- **Labs and CI:** containerlab · EVE-NG · Docker · GitHub Actions · Jenkins

## Say hello

Want to talk shop about multi-vendor edge cases, Nautobot, or network data modeling? Open an issue on any repository above.
