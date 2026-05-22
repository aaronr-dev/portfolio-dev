<svelte:head><title>Experience — Aaron Rodriguez</title></svelte:head>
<script>
  const roles = [
    { company: 'National CineMedia (NCM)', title: 'Senior Data Engineer', date: 'May 2022 – Present', current: true, desc: 'Owns end-to-end pipeline architecture across Azure Databricks, ADF, Fivetran, and SSIS. Maintains a critical master pipeline whose completion triggers automated Power BI refreshes for executive, sales, and finance stakeholders. Manages DSP/SSP vendor integrations with The Trade Desk, Xandr, OpenX, and PubMatic. Leads Agile ceremonies via Azure DevOps.' },
    { company: 'Insight Global (AT&T, Contractor)', title: 'Senior BI Developer', date: 'Mar 2022 – May 2022', desc: 'Developed SSAS tabular models, DAX measures, and Power BI Premium reports for enterprise reporting. Recruited directly by NCM before contract end.' },
    { company: 'Provisions Group', title: 'Senior Data Engineer', date: 'Sep 2021 – Mar 2022', desc: 'Designed SSAS tabular models and Power BI semantic layers with row-level security. Built end-to-end ETL pipelines from relational databases, flat files, and APIs into centralized warehouse layers.' },
    { company: 'ExactCare Pharmacy', title: 'BI Developer III', date: 'Mar 2021 – Sep 2021', desc: 'Built ADF pipelines and dimensional models supporting executive Power BI dashboards, cutting warehouse query time by 15%. Replaced legacy SSRS with governed Power BI paginated reports.' },
    { company: 'TruGreen', title: 'BI Developer', date: 'Mar 2020 – Oct 2020', desc: 'Designed star schema models and SSAS tabular models. Migrated 20+ enterprise Tableau reports to Power BI. Conducted code reviews for a 6-person development team.' },
    { company: 'MAA', title: 'Senior Data Engineer / Senior BI Developer', date: 'May 2019 – Mar 2021', desc: 'Automated marketing data pipelines with Python and the Google Reporting API, cutting processing time by 25%. Rewrote slow T-SQL scripts improving performance by 20%.' },
    { company: 'JuicePlus+', title: 'Data Engineer', date: 'May 2018 – May 2019', desc: 'Built data integration pipelines from Oracle to SQL Server with SSAS tabular models and row-level security, increasing operational efficiency by 30%.' },
    { company: 'Ring Container Technologies', title: 'BI Developer', date: 'Apr 2017 – May 2018', desc: 'Modernized SSIS workflows and deployed SSRS reports across 15 projects. Established Power BI and SSAS data security models.' },
    { company: 'Power & Tel Supply', title: 'BI Developer', date: 'May 2015 – Apr 2017', desc: 'Delivered BI solutions using Power BI, SSAS, and Phocas Software across distribution operations.' },
    { company: 'International Paper (Contract)', title: 'Application Developer III', date: 'Mar 2013 – May 2015', desc: 'Delivered application development and upgrade projects using T-SQL, SSIS, and C#.' },
    { company: 'Tec-Masters Inc.', title: 'Database & Reporting Engineer', date: 'Sep 2002 – Aug 2012', desc: 'Designed and maintained database-driven systems supporting enterprise logistics and reporting for government program stakeholders over a decade.' },
  ];
</script>
<div class="page-header">
  <h1>Experience</h1>
  <span class="count">{roles.length} roles · 2002–present</span>
</div>
<div class="roles">
  {#each roles as role}
    <div class="role" class:current={role.current}>
      <div class="role-left">
        <div class="date">{role.date}</div>
        <div class="company">{role.company}</div>
        {#if role.current}<span class="badge">Current</span>{/if}
      </div>
      <div class="role-right">
        <div class="title">{role.title}</div>
        <p>{role.desc}</p>
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
      <p>Deployed to Iraq in 2004 with I MEF, Al-Anbar Province, in support of OIF II. Previously held Secret clearance. National Defense Service Medal; Global War On Terrorism Service Medal; Global War On Terrorism Expeditionary Medal; Selected Marine Corps Reserve Medal.</p>
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
  .role.current { border-left: 3px solid var(--teal); }
  .role.mil { border-left: 3px solid #f59e0b; background: rgba(245,158,11,0.06); }
  .role.mil:hover { background: rgba(245,158,11,0.1); }
  .role-left { display: flex; flex-direction: column; gap: 0.3rem; }
  .date { font-family: var(--mono); font-size: 0.68rem; color: var(--muted); }
  .company { font-size: 0.85rem; font-weight: 600; color: var(--text); line-height: 1.4; }
  .badge { width: fit-content; background: var(--teal-dim); color: var(--teal); font-family: var(--mono); font-size: 0.6rem; letter-spacing: 0.06em; padding: 0.15rem 0.5rem; border-radius: 3px; margin-top: 0.25rem; }
  .role-right { display: flex; flex-direction: column; gap: 0.5rem; }
  .title { font-size: 0.88rem; font-weight: 600; color: var(--teal); }
  .mil-title { color: #f59e0b; }
  p { font-size: 0.85rem; color: var(--muted); line-height: 1.75; }
</style>
