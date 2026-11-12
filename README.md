# OfWolfAndMan

*I will either find a way, or I will make one.*

I build network automation, the kind that can say whether a device is already correct
rather than just pushing commands at it. Mostly Ansible and Python, mostly Cisco and Arista.

## What I'm working on

### [Automate teh Network](https://github.com/OfWolfAndMan/Automate-teh-Network)

Intent-based automation for Cisco IOS, Cisco NX-OS and Arista EOS. It replaces a 2017-era
pile of Python 2.7 playbooks that rendered whole device configurations and pushed them as
lines.

- **State, not commands.** Playbooks declare state through resource modules, so a second run
  answers the only question that matters: is the device already correct?
- **Compliance as data.** Policies are validated YAML, checked against saved device
  configurations, and the check runs with no hardware at all.
- **Honest status labels.** Every playbook says whether it was verified, partly verified, or
  never run beyond a syntax check, and the test run fails if the README drifts from that.
- **Nothing sensitive in a public repo.** A scrub, enforced in CI, keeps real credentials
  and addresses out.
- **A tutorial for people who have never used Ansible.** No network hardware needed.

## Other projects

- [chsheets](https://github.com/OfWolfAndMan/chsheets): cheat sheets, from OS-specific
  security configurations to scripting references and red/blue team scripts.
- [EVE-NG_Pipeline](https://github.com/OfWolfAndMan/EVE-NG_Pipeline): build, and tear down,
  a whole EVE-NG lab through its REST API, driven from Jenkins.
- [CCIE-Lab-Automation](https://github.com/OfWolfAndMan/CCIE-Lab-Automation): configure
  Cisco routers and switches from scratch on IOSv and CSR1000V, then back them up and
  collect diagnostics.

## Retired on purpose

Two older course repositories, [Network-Automation-Mini-Course](https://github.com/OfWolfAndMan/Network-Automation-Mini-Course)
and [NotLayer3-NetworkAutomation](https://github.com/OfWolfAndMan/NotLayer3-NetworkAutomation),
are archived. What was worth keeping was ported into Automate teh Network, and every file
there has either a successor or a written reason it was left behind.

## Toolbox

Ansible (resource modules, roles, Ansible Vault) · Python (Netmiko, ntc-templates, Jinja2,
Flask, pytest, ruff) · Cisco IOS and NX-OS · Arista EOS · containerlab and EVE-NG · Docker ·
GitHub Actions

## How I work

- A claim is current only if it was executed.
- Nothing published carries a real credential, address or name.
- Retirements are written down, with reasons.

## Say hello

Open an issue on any repository above.
