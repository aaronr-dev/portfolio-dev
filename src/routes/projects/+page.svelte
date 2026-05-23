<svelte:head><title>Projects — Aaron Rodriguez</title></svelte:head>
<script>
  const projects = [
    { name: 'Box Office Analytics Pipeline', status: 'Live', desc: 'End-to-end analytics pipeline over 50 years of US domestic box office data, 9,000+ films from 1976 to present. Python web scraper, PySpark processing, dbt modeling, Evidence.dev reporting layer.', stack: ['Python', 'PySpark', 'dbt', 'Evidence.dev', 'Linux'] },
    { name: 'YNAB Analytics Pipeline', status: 'Live', desc: 'Personal finance pipeline pulling from the YNAB API, modeled with dbt, deployed via Vercel. Production-quality infrastructure built for real budget visibility.', stack: ['YNAB API', 'Python', 'dbt', 'Vercel'] },
    { name: 'Snowflake Personal Lab', status: 'In progress', desc: 'Building a production-quality Snowflake pipeline with streams, tasks, dynamic tables, and Snowpark. Documenting the build as I go.', stack: ['Snowflake', 'dbt', 'Python', 'Snowpark'] },
  ];
</script>
<div class="page-header"><h1>Projects</h1></div>
<div class="projects">
  {#each projects as project, i}
    <div class="project">
      <div class="project-top">
        <span class="num">0{i+1}</span>
        <span class="status" class:live={project.status === 'Live'}>{project.status}</span>
      </div>
      <div class="name">{project.name}</div>
      <p>{project.desc}</p>
      <div class="stack">{#each project.stack as tag}<span class="tag">{tag}</span>{/each}</div>
    </div>
  {/each}
</div>
<style>
  .page-header { margin-bottom: 1.5rem; }
  h1 { font-size: 1.5rem; font-weight: 600; letter-spacing: -0.02em; }
  .projects { display: flex; flex-direction: column; gap: 1rem; }
  .project { background: var(--bg2); border: 1px solid rgba(255,255,255,0.06); border-left: 4px solid var(--teal); border-radius: 8px; padding: 1.75rem; display: flex; flex-direction: column; gap: 0.85rem; transition: background 0.15s; }
  .project:hover { background: var(--bg3); }
  .project-top { display: flex; justify-content: space-between; align-items: center; }
  .num { font-family: var(--mono); font-size: 0.68rem; color: var(--muted); }
  .status { font-family: var(--mono); font-size: 0.62rem; letter-spacing: 0.05em; padding: 0.2rem 0.65rem; border-radius: 4px; background: rgba(255,255,255,0.06); color: var(--muted); }
  .status.live { background: rgba(20,184,166,0.15); color: var(--teal); }
  .name { font-size: 1.05rem; font-weight: 600; color: var(--text); }
  p { font-size: 0.88rem; color: var(--muted); line-height: 1.75; max-width: 62ch; }
  .stack { display: flex; flex-wrap: wrap; gap: 0.4rem; }
  .tag { font-family: var(--mono); font-size: 0.67rem; color: var(--teal); background: var(--teal-dim); padding: 0.2rem 0.6rem; border-radius: 4px; }
</style>
