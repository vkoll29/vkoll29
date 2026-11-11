<h1 align="center">Hi, I'm George 👋</h1>

<p align="center">
  <b>Data engineer with a cloud infrastructure background.</b><br/>
  I build data platforms from the ground up: the network and servers, the databases, and the pipelines on top.
</p>

<p align="center">
  <img alt="Microsoft Azure" src="https://img.shields.io/badge/Microsoft_Azure-0078D4?style=flat-square"/>
  <img alt="Linux" src="https://img.shields.io/badge/Linux-333333?style=flat-square&logo=linux&logoColor=white"/>
  <img alt="Terraform" src="https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white"/>
  <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img alt="GitHub Actions" src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white"/>
  <br/>
  <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
  <img alt="SQL" src="https://img.shields.io/badge/SQL-4479A1?style=flat-square"/>
  <img alt="Apache Airflow" src="https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white"/>
  <img alt="Cloudflare" src="https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white"/>
</p>

---

## ☁️ Cloud and data infrastructure

**Now: PostgreSQL and Linux in production.** My focus these days is databases and the data flowing through them: keeping it fast, reliable, and worth trusting.

**Before: Azure, across the whole stack.** I designed, built and ran data platforms on Azure, from architecture and networking through administration to data engineering.

- **Architecture and networking.** Environments designed end to end: virtual networks, subnets and network security groups, identity and access through Entra ID, and compute and storage sized to the workload and to the budget.
- **Infrastructure as code.** Whole environments defined in Terraform (`azurerm`, `azuread`): resource groups, ADLS Gen2 lakes, VNets, Linux VMs with managed disks and scheduled auto-shutdown, and the service principals the pipelines authenticate as.
- **Data platforms.** Data lakes on ADLS Gen2, event-driven ingestion with Azure Functions blob triggers, tooling to audit lake contents at scale, and ETL in Python and SQL feeding reporting databases and dashboards.

## ⚡ Side project: Kenya Power Tracker

<table>
  <tr>
    <td width="270" valign="top">
      <a href="https://t.me/kplc_tracker_bot"><img src="assets/kplc-tracker-bot.jpeg" alt="The Kenya Power Tracker bot listing upcoming outages by region and area in Telegram" width="250"/></a>
    </td>
    <td valign="top">
      <p>Kenya Power publishes planned outages as PDFs that nobody can search or subscribe to. This project reads every notice each hour, turns it into structured data (1,400+ outages parsed so far in 2026), and serves it through a Telegram bot.</p>
      <p>Follow your area with <code>/subscribe</code> and the bot messages you when a new notice lists it. Matching is fuzzy enough to catch KPLC's spellings ("Dagoretti" finds "Dagoreti").</p>
      <p>It runs entirely on free tiers.</p>
      <p><b>Try it:</b> <a href="https://t.me/kplc_tracker_bot">@kplc_tracker_bot</a></p>
      <p><i>Python · pdfplumber · GitHub Actions · Cloudflare Workers + D1</i></p>
    </td>
  </tr>
</table>

```mermaid
flowchart LR
    kplc[("kplc.co.ke<br/>PDF notices")] -->|hourly| ingest["Ingest job<br/>GitHub Actions"]
    ingest -->|"extract + parse"| d1[("Cloudflare D1")]
    d1 --> bot["Telegram bot<br/>Cloudflare Worker"]
    bot -->|"alerts for areas you follow"| users(["Subscribers"])
```

---

- 👯 Open to collaborating on data engineering and cloud infrastructure work
- 💬 Ask me about Azure, PostgreSQL in production, Terraform, and parsing messy documents into clean data

<p align="center">
  <img src="./profile/stats.svg" alt="George's GitHub stats" height="170"/>
  <img src="./profile/top-langs.svg" alt="Most used languages" height="170"/>
</p>
