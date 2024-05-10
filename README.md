# auditd-mitre-attack
Linux Audit Rules attributed to [MITRE ATT\&CK](https://attack.mitre.org/matrices/enterprise/linux/) framework techniques & subtechniques.

## Content
Rules are split into files per the framework tactics. Detections are in place for the following:

TBD

## Installation
1. Tailor the ruleset as needed and deploy to `/etc/audit/rules.d`.
2. Run `augenrules --load` and check for syntax errors.
3. Reboot the host.

## Usage
All rules are assigned a filter key: `ATTACK_` + `<technique_code>` (+ `_<subtechnique_number>` if applicable)

E.g. to search for events under *Install Root Certificate* subtechnique (T1553.004), use:

```
ausearch -k ATTACK_T1553_004
```
