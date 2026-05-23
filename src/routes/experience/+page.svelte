<svelte:head><title>Experience — Aaron Rodriguez</title></svelte:head>
<script>
  const roles = [
    { company: 'National CineMedia (NCM)', title: 'Senior Data Engineer', date: 'May 2022 – May 2026', current: false, desc: [
      'Proactively identified duplicate records causing Power BI refresh failures via daily monitoring, implementing pipeline deduplication logic that prevented recurrence for 10-15 executive, sales, and finance stakeholders.',
      'Resolved a critical production outage in under a day after a vendor deleted upstream tables, reconstructed SQL logic, validated data integrity end-to-end, and prevented a full reporting blackout across the organization.',
      'Maintained and extended a metadata-driven Databricks architecture that leverages dynamic SQL to generate dimension and fact tables from centralized Azure SQL Database logic, enabling scalable, configuration-driven pipeline execution across the data lake.',
      'Managed DSP/SSP vendor data quality across Fivetran integrations with The Trade Desk, Xandr, OpenX, and PubMatic, triaging CSV anomalies and restoring clean feeds within 1.5 days of escalation.',
      'Built a net-new ADF and Databricks pipeline aggregating 200M+ rows into a daily incremental Power BI dashboard surfacing circuit share revenue opportunities for the sales team, with sub-20-minute pipeline runtime.',
      'Diagnosed and resolved a CI/CD blockage by reconfiguring broken build agents, restoring deployments across Dev, Test, and Prod.'
    ]},
    { company: 'Insight Global (AT&T, Contractor)', title: 'Senior BI Developer', date: 'Mar 2022 – May 2022', desc: [
      'Filled a critical reporting gap for AT&T retail stores by delivering SSAS tabular models, DAX measures, and Power BI Premium dashboards that gave store teams visibility into their performance metrics for the first time.',
      'Recruited directly by National CineMedia before contract end.'
    ]},
    { company: 'Provisions Group', title: 'Senior Data Engineer', date: 'Sep 2021 – Mar 2022', desc: [
      'Consulted across multiple clients conducting Power BI POCs that drove adoption of the Power BI ecosystem as the primary reporting platform.',
      'Designed and built a large-scale healthcare data warehouse with a raw layer, stored procedures encapsulating business logic, and destination tables aggregated through SSAS tabular models and Power BI reports.'
    ]},
    { company: 'ExactCare Pharmacy', title: 'BI Developer III', date: 'Mar 2021 – Sep 2021', desc: [
      'Built ADF pipelines from source to raw landing zone, with stored procedures generating facts and dimensions across multiple data marts powering Power BI reporting.',
      'Improved warehouse query performance by 15% through stored procedure tuning.',
      'Developed SSRS reports for clinical and operational stakeholders.'
    ]},
    { company: 'MAA (Recruited Back)', title: 'Senior BI Developer', date: 'Oct 2020 – Mar 2021', desc: [
      'Built and maintained Power BI reports and SSAS tabular models with DAX measures and row-level security, delivering self-serve analytics to property management and executive stakeholders.',
      'Built SQL and SSRS reports that gave leadership the operational visibility they were missing.'
    ]},
    { company: 'TruGreen', title: 'BI Developer', date: 'Mar 2020 – Oct 2020', desc: [
      'Migrated 30+ Tableau reports to Power BI, consolidating multiple reports into single unified dashboards and improving the reporting experience across finance and operations teams.',
      'Built star schema data models and SSAS tabular models supporting self-serve analytics across billions of rows of enterprise data.',
      'Conducted code reviews and provided technical guidance to a 6-person development team, enforcing data modeling standards and best practices.'
    ]},
    { company: 'MAA', title: 'Senior Data Engineer', date: 'May 2019 – Mar 2020', desc: [
      'Built a net-new Python pipeline pulling campaign performance, spend, and impression data from the Google Reporting API into SQL Server facts and dimensions, giving the marketing team their first visibility into campaign analytics via Power BI.',
      'Identified and resolved slow indexes through index analysis and tuning, improving stored procedure and query performance across high-volume production databases.'
    ]},
    { company: 'JuicePlus+', title: 'Data Engineer', date: 'May 2018 – May 2019', desc: [
      'Led a large-scale POC effort to evaluate and demonstrate Power BI capabilities across sales and operations, resulting in company-wide adoption of Power BI as the primary reporting platform.',
      'Built a net-new SQL Server data warehouse sourced from Oracle via SSIS pipelines, including SSAS tabular models and Power BI reports covering sales and operational reporting across the organization.',
      'Proactively developed Power BI mobile reports as part of the POC effort to showcase platform capabilities and drive stakeholder buy-in.'
    ]},
    { company: 'Ring Container Technologies', title: 'BI Developer', date: 'Apr 2017 – May 2018', desc: [
      'Built net-new SSIS pipelines ingesting data from flat files, Excel, and SQL Server into star schema data marts covering asset management, sales, and CRM.',
      'Designed and built Power BI dashboards with DAX measures, Power Query transformations, and row-level security across multiple business domains.',
      'Developed 20+ parameterized SSRS reports with scheduled execution and email delivery to executive staff, with PDF and Excel export formats.'
    ]},
    { company: 'Power & Tel Supply', title: 'BI Developer', date: 'May 2015 – Apr 2017', desc: [
      'Filled a critical reporting gap for a wholesale telecom distributor by building net-new SSIS pipelines extracting data from Progress OpenEdge into SQL Server staging tables and loading into a data warehouse.',
      'Led adoption of Power BI as the primary reporting platform, designing complex data models in Power BI and SSAS with DAX measures, calculated columns, and row-level security.'
    ]},
    { company: 'International Paper (Contract)', title: 'Application Developer III', date: 'Mar 2013 – May 2015', desc: [
      'Delivered application development and upgrade projects using T-SQL, SSIS, and C#, coordinating system changes in alignment with organizational requirements.',
      'Collaborated with packaging clients, consultants, and end users to gather and translate application requirements into technical specifications.'
    ]},
    { company: 'Tec-Masters Inc.', title: 'Database & Reporting Engineer', date: 'Sep 2002 – Aug 2012', desc: [
      'Designed and maintained database-driven systems supporting enterprise logistics, operations, and reporting for defense program stakeholders over a decade.',
      'Built automated SQL pipelines and scheduled jobs that kept nightly data processing running reliably for over 10 years.',
      'Established early version control, automation, and documentation practices for long-running production workflows, habits that have carried through every role since.'
    ]},
  ];
</script>
<div class="page-header">
  <h1>Experience</h1>
  <span class="count">{roles.length} roles · 2002–2026</span>
</div>
<div class="roles">
  {#each roles as role}
    <div class="role">
      <div class="role-left">
        <div class="date">{role.date}</div>
        <div class="company">{role.company}</div>
      </div>
      <div class="role-right">
        <div class="title">{role.title}</div>
        <ul>
          {#each role.desc as bullet}
            <li>{bullet}</li>
          {/each}
        </ul>
      </div>
    </div>
  {/each}
  <div class="role mil">
    <div class="role-left">
      <div class="date">Oct 2001 – 2005</div>
      <div class="company">US Marine Corps Reserve</div>
    </div>
    <div class="role-right">
      <div class="title mil-title">Field Artillery Cannoneer (0811)</div>
      <ul>
        <li>Deployed to Iraq in 2004 with I MEF, Al-Anbar Province, in support of OIF II. Previously held Secret clearance.</li>
        <li>National Defense Service Medal; Global War On Terrorism Service Medal; Global War On Terrorism Expeditionary Medal; Selected Marine Corps Reserve Medal.</li>
      </ul>
    </div>
  </div>
</div>
<style>
  .page-header { display: flex; align-items: baseline; justify-content: space-between; margin-bottom: 1.5rem; }
  h1 { font-size: 1.5rem; font-weight: 600; letter-spacing: -0.02em; }
  .count { font-family: var(--mono); font-size: 0.72rem; color: var(--muted); }
  .roles { display: flex; flex-direction: column; border-radius: 8px; overflow: hidden; border: 1px solid rgba(255,255,255,0.06); }
  .role { display: grid; grid-template-columns: 195px 1fr; gap: 1.5rem; padding: 1.5rem; background: var(--bg2); border-bottom: 1px solid rgba(255,255,255,0.05); transition: background 0.15s; }
  .role:last-child { border-bottom: none; }
  .role:hover { background: var(--bg3); }
  .role.mil { border-left: 3px solid #f59e0b; background: rgba(245,158,11,0.06); }
  .role.mil:hover { background: rgba(245,158,11,0.1); }
  .role-left { display: flex; flex-direction: column; gap: 0.3rem; }
  .date { font-family: var(--mono); font-size: 0.68rem; color: var(--muted); }
  .company { font-size: 0.85rem; font-weight: 600; color: var(--text); line-height: 1.4; }
  .role-right { display: flex; flex-direction: column; gap: 0.5rem; }
  .title { font-size: 0.88rem; font-weight: 600; color: var(--teal); margin-bottom: 0.4rem; }
  .mil-title { color: #f59e0b; }
  ul { padding-left: 1rem; display: flex; flex-direction: column; gap: 0.4rem; }
  li { font-size: 0.85rem; color: var(--muted); line-height: 1.75; }
</style>
