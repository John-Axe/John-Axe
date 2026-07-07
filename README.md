<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Orbitron&weight=900&size=40&duration=3000&pause=1000&color=C084FC&center=true&vCenter=true&width=800&height=100&lines=JO%C3%83O+MACHADO)](https://git.io/typing-svg)

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Share+Tech+Mono&weight=700&size=19&duration=2000&pause=800&color=C084FC&center=true&vCenter=true&width=800&lines=THREAT+HUNTER+//+DETECTION+ENGINEER+//+DFIR;TRIAGING+EDR+%2B+NIDS+%2B+EMAIL;ENGINEERING+DETECTIONS+THAT+FIRE;DANGEROUS+WITH+PYTHON;BAY+AREA+CA)](https://git.io/typing-svg)

<br/>

![](https://img.shields.io/badge/%E2%9A%A1%20SOC-ACTIVE-6D28D9?style=for-the-badge&labelColor=1a0033)
![](https://img.shields.io/badge/%F0%9F%8E%AF%20THREAT-HUNTER-7C3AED?style=for-the-badge&labelColor=1a0033)
![](https://img.shields.io/badge/%F0%9F%94%8D%20DFIR-DEPLOYED-A855F7?style=for-the-badge&labelColor=1a0033)
![](https://img.shields.io/badge/%F0%9F%9B%A1%EF%B8%8F%20DETECTION-ENG-9333EA?style=for-the-badge&labelColor=1a0033)

</div>

---

## <img src="https://media.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif" width="28"/> &nbsp;WHO'S THERE

```css
name     →  João Machado  //  John-Axe
base     →  San Francisco Bay Area, CA
langs    →  English · Portuguese · Spanish
mission  →  hunt threats · build detections · respond fast
```

> I hunt threats. I build detections that actually fire.
> I dig into the alerts others skip.
> Fluent in logs. Dangerous with Python.
> **Zero chill when something looks wrong.**

---

## <img src="https://media.giphy.com/media/26u4cqiYI30juCOGY/giphy.gif" width="28"/> &nbsp;SECURITY ENGINEERING ECOSYSTEM

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Share+Tech+Mono&weight=700&size=16&duration=2200&pause=800&color=C084FC&center=true&vCenter=true&width=800&lines=14+TOOLS+//+1+SHARED+SCHEMA+//+1+DASHBOARD;NOT+A+FOLDER+OF+SCRIPTS.+AN+ECOSYSTEM.)](https://git.io/typing-svg)

```
▸ every tool speaks the same language.

  dlp-secret-pii-scanner  ─┐
  detection-as-code       ─┤
  iam-privesc-mapper      ─┼──▶  finding-schema  ──▶  observability-stack  ──▶  Grafana
  aws-auto-remediation    ─┤      (JSON Schema +        (Loki + Promtail,         dashboard
  8× tier-2 script tools  ─┘       Pydantic model)        $0, local-only)
```

14 repos, tiered by real maturity, wired together by one shared finding shape instead of 14 bespoke parsers. Every tool below either runs in CI or ships a `--emit-findings` flag validated against real output — not a demo built for screenshots.

<details>
<summary><b>🔓 dlp-secret-pii-scanner</b> &nbsp;·&nbsp; <img src="https://img.shields.io/badge/LIVE-CI%20%2B%20FUZZED-6D28D9?style=flat-square&labelColor=0D0D0D"/> &nbsp;<code>secrets · PII · CI gate</code></summary>
<br/>

```
▸ zero deps. finds the key before it ships.
```

Secret/PII scanner with a pre-commit hook, a benchmark suite, fuzzing, and a `SECURITY.md`. Its `action.yml` is a reusable GitHub Action — I reuse it as the secret-scanning CI gate across my other flagship repos instead of writing the same step four times.

![](https://img.shields.io/badge/Python-grey?style=flat-square&logo=python&logoColor=3776AB)
![](https://img.shields.io/badge/Fuzzing-grey?style=flat-square)
![](https://img.shields.io/badge/GitHub_Actions-grey?style=flat-square&logo=githubactions&logoColor=2088FF)
![](https://img.shields.io/badge/Pre--commit-grey?style=flat-square)

**[→ VIEW REPO](https://github.com/John-Axe/dlp-secret-pii-scanner)**

<br/>
</details>

<details>
<summary><b>🎯 detection-as-code</b> &nbsp;·&nbsp; <img src="https://img.shields.io/badge/LIVE-HARDENED-7C3AED?style=flat-square&labelColor=0D0D0D"/> &nbsp;<code>Sigma rules · testing · scorecard</code></summary>
<br/>

```
▸ detections that are tested like code, because they are code.
```

Sigma detection rules with an actual test suite behind them, plus OpenSSF Scorecard hardening. The consolidation point for signal coming out of the tier-2 tools below.

![](https://img.shields.io/badge/Sigma_Rules-grey?style=flat-square)
![](https://img.shields.io/badge/Python-grey?style=flat-square&logo=python&logoColor=3776AB)
![](https://img.shields.io/badge/OpenSSF_Scorecard-grey?style=flat-square)
![](https://img.shields.io/badge/CI-grey?style=flat-square&logo=githubactions&logoColor=2088FF)

**[→ VIEW REPO](https://github.com/John-Axe/detection-as-code)**

<br/>
</details>

<details>
<summary><b>🔑 iam-privesc-mapper</b> &nbsp;·&nbsp; <img src="https://img.shields.io/badge/LIVE-16%20FINDINGS%20VERIFIED-A855F7?style=flat-square&labelColor=0D0D0D"/> &nbsp;<code>IAM · privesc graph · MITRE ATT&CK</code></summary>
<br/>

```
▸ maps how a low-priv role becomes admin.
```

Builds an IAM privilege-escalation graph from Terraform/account data and maps each technique to real MITRE ATT&CK Cloud IDs (`T1098.003`, `T1548.005`, `T1078.004`). Fuzz-tested; ran against a real 16-finding sample account, not synthetic fixtures.

![](https://img.shields.io/badge/Python-grey?style=flat-square&logo=python&logoColor=3776AB)
![](https://img.shields.io/badge/Terraform-grey?style=flat-square&logo=terraform&logoColor=844FBA)
![](https://img.shields.io/badge/MITRE_ATT%26CK-grey?style=flat-square)
![](https://img.shields.io/badge/Fuzzing-grey?style=flat-square)

**[→ VIEW REPO](https://github.com/John-Axe/iam-privesc-mapper)**

<br/>
</details>

<details>
<summary><b>⚡ aws-auto-remediation</b> &nbsp;·&nbsp; <img src="https://img.shields.io/badge/LIVE-DEPLOYED%20%26%20TORN%20DOWN-9333EA?style=flat-square&labelColor=0D0D0D"/> &nbsp;<code>Lambda · EventBridge · Terraform</code></summary>
<br/>

```
▸ CloudTrail event in. remediation out. no idle infra.
```

Terraform-defined Lambda + EventBridge auto-remediation, with CI and lockfile automation. Recorded a live AWS demo, then `terraform destroy` — under $2 total, nothing left running.

![](https://img.shields.io/badge/Terraform-grey?style=flat-square&logo=terraform&logoColor=844FBA)
![](https://img.shields.io/badge/AWS_Lambda-grey?style=flat-square&logo=awslambda&logoColor=FF9900)
![](https://img.shields.io/badge/EventBridge-grey?style=flat-square)
![](https://img.shields.io/badge/CI%2FCD-grey?style=flat-square)

**[→ VIEW REPO](https://github.com/John-Axe/aws-auto-remediation)**

<br/>
</details>

<details>
<summary><b>🧩 finding-schema + observability-stack</b> &nbsp;·&nbsp; <img src="https://img.shields.io/badge/LIVE-THE%20GLUE-C084FC?style=flat-square&labelColor=0D0D0D"/> &nbsp;<code>JSON Schema · Grafana · Loki</code></summary>
<br/>

```
▸ build the parser once. every tool speaks it.
```

A miniature OCSF/Security-Hub-style finding shape (`id`, `source`, `severity`, `category`, `mitre_attack`, `owasp`, `remediation`, `raw`) plus a $0-cost local Grafana + Loki + Promtail stack that ingests every tool's output into one Findings Overview dashboard. This is what turns 14 repos into one ecosystem instead of a repo list.

![](https://img.shields.io/badge/JSON_Schema-grey?style=flat-square)
![](https://img.shields.io/badge/Pydantic-grey?style=flat-square)
![](https://img.shields.io/badge/Grafana-grey?style=flat-square&logo=grafana&logoColor=F46800)
![](https://img.shields.io/badge/Loki-grey?style=flat-square)

**[→ VIEW SCHEMA](https://github.com/John-Axe/finding-schema)** &nbsp;·&nbsp; **[→ VIEW STACK](https://github.com/John-Axe/observability-stack)**

<br/>
</details>

<details>
<summary><b>🛰️ Tier-2 Arsenal</b> &nbsp;·&nbsp; <img src="https://img.shields.io/badge/LIVE-8%2F10%20WIRED-6D28D9?style=flat-square&labelColor=0D0D0D"/> &nbsp;<code>recon · network · host · appsec</code></summary>
<br/>

```
▸ single-purpose tools. 8 of them already feed the schema above.
```

`port-scanner` + `packet-sniffer` feed `intrusion-detection-system`. `file-integrity-monitor` + `keylogger-detector` cover host telemetry. `web-vuln-scanner` + `phishing-detector` cover appsec and social. `firewall-simulator` closes the loop on enforcement. Plus two standalone crypto/auth demonstrations kept deliberately *out* of the pipeline — `encrypted-chat` (RSA-2048 + AES-256-GCM) and `password-cracker` (dictionary / brute-force / rainbow-table) — forcing them in would be the same credibility problem as over-selling a thin repo.

![](https://img.shields.io/badge/Python-grey?style=flat-square&logo=python&logoColor=3776AB)
![](https://img.shields.io/badge/Scapy-grey?style=flat-square)
![](https://img.shields.io/badge/Sockets-grey?style=flat-square)
![](https://img.shields.io/badge/Flask-grey?style=flat-square&logo=flask&logoColor=white)

**[→ port-scanner](https://github.com/John-Axe/port-scanner)** · **[→ packet-sniffer](https://github.com/John-Axe/packet-sniffer)** · **[→ intrusion-detection-system](https://github.com/John-Axe/intrusion-detection-system)** · **[→ firewall-simulator](https://github.com/John-Axe/firewall-simulator)** · **[→ file-integrity-monitor](https://github.com/John-Axe/file-integrity-monitor)** · **[→ keylogger-detector](https://github.com/John-Axe/keylogger-detector)** · **[→ web-vuln-scanner](https://github.com/John-Axe/web-vuln-scanner)** · **[→ phishing-detector](https://github.com/John-Axe/phishing-detector)** · **[→ encrypted-chat](https://github.com/John-Axe/encrypted-chat)** · **[→ password-cracker](https://github.com/John-Axe/password-cracker)**

<br/>
</details>

---

## <img src="https://media.giphy.com/media/iIqmM5tTjmpOB9mpbn/giphy.gif" width="28"/> &nbsp;PERSONAL LABS

<details>
<summary><b>☁️ AWS Network Firewall</b> &nbsp;·&nbsp; <img src="https://img.shields.io/badge/LIVE-DEPLOYED-6D28D9?style=flat-square&labelColor=0D0D0D"/> &nbsp;<code>network security · cloud · firewall</code></summary>
<br/>

```
▸ build it. break it. understand every packet.
```

Configured AWS Network Firewall from scratch — stateful inspection rule groups, traffic filtering logic, and behavioral testing to understand exactly how traffic gets allowed, blocked, and logged.

![](https://img.shields.io/badge/AWS-grey?style=flat-square&logo=amazonaws&logoColor=FF9900)
![](https://img.shields.io/badge/Network_Security-grey?style=flat-square)
![](https://img.shields.io/badge/Firewall_Rules-grey?style=flat-square)
![](https://img.shields.io/badge/Cloud_Security-grey?style=flat-square)

**[→ VIEW LAB](https://github.com/John-Axe/AWS/blob/d39f397536cd19ae2a34ae6037a1a199221b6d5c/AWS-Labs/Configure-AWS-Network-Firewall/README.md)**

<br/>
</details>

<details>
<summary><b>🐍 100 Days of Python</b> &nbsp;·&nbsp; <img src="https://img.shields.io/badge/LIVE-ACTIVE-6D28D9?style=flat-square&labelColor=0D0D0D"/> &nbsp;<code>scripting · automation · security tooling</code></summary>
<br/>

```
▸ ship something every day. automate everything eventually.
```

100 consecutive days of building — automation scripts, security utilities, and tools from scratch. Less tutorial, more hands-on problem solving.

![](https://img.shields.io/badge/Python-grey?style=flat-square&logo=python&logoColor=3776AB)
![](https://img.shields.io/badge/Automation-grey?style=flat-square)
![](https://img.shields.io/badge/Scripting-grey?style=flat-square)
![](https://img.shields.io/badge/Security_Tooling-grey?style=flat-square)

**[→ VIEW PROJECTS](https://github.com/John-Axe/100-Days-of-Python-Projects)**

<br/>
</details>

<details>
<summary><b>🔵 Azure Security Lab</b> &nbsp;·&nbsp; <img src="https://img.shields.io/badge/STATUS-INCOMING-A855F7?style=flat-square&labelColor=0D0D0D"/> &nbsp;<code>SIEM · cloud · threat monitoring</code></summary>
<br/>

```
▸ sentinel. defender. detection pipelines. coming soon.
```

Building out a Microsoft Azure security lab focused on Sentinel detection rules, Defender for Endpoint, and threat monitoring pipelines.

![](https://img.shields.io/badge/Azure-grey?style=flat-square&logo=microsoftazure&logoColor=0089D6)
![](https://img.shields.io/badge/Microsoft_Sentinel-grey?style=flat-square)
![](https://img.shields.io/badge/SIEM-grey?style=flat-square)
![](https://img.shields.io/badge/Detection_Engineering-grey?style=flat-square)

<br/>
</details>

<details>
<summary><b>🗂️ Active Directory Attack &amp; Defense</b> &nbsp;·&nbsp; <img src="https://img.shields.io/badge/STATUS-INCOMING-A855F7?style=flat-square&labelColor=0D0D0D"/> &nbsp;<code>identity · attack sim · detection</code></summary>
<br/>

```
▸ understand the attack surface. build the detections. close the gaps.
```

Spinning up an AD lab to simulate common identity-based attacks — pass-the-hash, kerberoasting, enumeration — and engineering detections to catch them.

![](https://img.shields.io/badge/Active_Directory-grey?style=flat-square)
![](https://img.shields.io/badge/Attack_Simulation-grey?style=flat-square)
![](https://img.shields.io/badge/Detection_Engineering-grey?style=flat-square)
![](https://img.shields.io/badge/Windows-grey?style=flat-square&logo=windows)

<br/>
</details>

---

<div align="center">

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=John-Axe&bg_color=0d0d0d&color=C084FC&line=7C3AED&point=ffffff&area=true&area_color=6D28D9&hide_border=false&border_color=9333EA&radius=6&custom_title=ACTIVITY+TRACE)](https://github.com/John-Axe)

</div>

---

## <img src="https://media.giphy.com/media/WUlplcMpOCEmTGBtBW/giphy.gif" width="28"/> &nbsp;CERTS INCOMING

<div align="center">

![](https://img.shields.io/badge/CompTIA-Security%2B-C084FC?style=for-the-badge&logo=comptia&logoColor=white&labelColor=1a0033)
![](https://img.shields.io/badge/CompTIA-Network%2B-9333EA?style=for-the-badge&logo=comptia&logoColor=white&labelColor=1a0033)
![](https://img.shields.io/badge/AWS-Cloud_Practitioner-A855F7?style=for-the-badge&logo=amazonaws&logoColor=white&labelColor=1a0033)

<br/>

```
  Security+        ████████████████░░░░  july 2026
  Network+         ██████████████░░░░░░  july 2026
  AWS Practitioner ████████████░░░░░░░░  july 2026
```

</div>

---

## <img src="https://media.giphy.com/media/cIn5fTcjnuqqg/giphy.gif" width="28"/> &nbsp;DIAGNOSTICS

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com?user=John-Axe&theme=radical&background=0D0D0D&border=7C3AED&ring=C084FC&fire=A855F7&currStreakLabel=C084FC&sideLabels=A855F7&dates=6D28D9)](https://github.com/John-Axe)

[![João's GitHub Stats](https://github-readme-stats.vercel.app/api?username=John-Axe&show_icons=true&theme=radical&bg_color=0D0D0D&border_color=7C3AED&title_color=C084FC&icon_color=A855F7&text_color=ffffff)](https://github.com/John-Axe)

</div>

---

## <img src="https://media.giphy.com/media/LnQjpWaON8nhr21vNW/giphy.gif" width="28"/> &nbsp;OPEN CHANNEL

<div align="center">

![](https://img.shields.io/badge/LIVE-DART%20INTERN%20%40%20ROBLOX-6D28D9?style=for-the-badge&labelColor=1a0033)

[![LinkedIn](https://img.shields.io/badge/LINKEDIN-CONNECT%20NOW-A855F7?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=1a0033)](https://www.linkedin.com/in/jplmachado/)

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20,24&height=120&section=footer&animation=fadeIn"/>

![](https://komarev.com/ghpvc/?username=John-Axe&color=9333EA&style=for-the-badge&label=PROFILES+SCANNED)

<br/><br/>

*`"defenders think in lists. attackers think in graphs. always be the graph."`*

</div>
