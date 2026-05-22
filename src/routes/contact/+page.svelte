<svelte:head><title>Contact — Aaron Rodriguez</title></svelte:head>
<div class="page-header"><h1>Contact</h1></div>
<div class="card">
  <a href="mailto:aaron@aaronr.dev" class="row">
    <span class="label">Email</span>
    <span class="value">aaron@aaronr.dev</span>
    <span class="arrow">→</span>
  </a>
  <a href="https://linkedin.com/in/aaronjrodriguez" target="_blank" rel="noopener" class="row">
    <span class="label">LinkedIn</span>
    <span class="value">linkedin.com/in/aaronjrodriguez</span>
    <span class="arrow">→</span>
  </a>
  <a href="https://github.com/ajrodr82" target="_blank" rel="noopener" class="row">
    <span class="label">GitHub</span>
    <span class="value">github.com/ajrodr82</span>
    <span class="arrow">→</span>
  </a>
  <a href="/AaronRodriguez_Resume_DE.pdf" target="_blank" class="row">
    <span class="label">Resume</span>
    <span class="value">Download PDF</span>
    <span class="arrow">→</span>
  </a>
</div>
<style>
  .page-header { margin-bottom: 1.5rem; }
  h1 { font-size: 1.5rem; font-weight: 600; letter-spacing: -0.02em; }
  .card { background: var(--bg2); border: 1px solid rgba(255,255,255,0.06); border-radius: 8px; overflow: hidden; }
  .row { display: grid; grid-template-columns: 110px 1fr auto; align-items: center; gap: 1rem; padding: 1.25rem 1.5rem; border-bottom: 1px solid rgba(255,255,255,0.05); color: var(--text); transition: background 0.15s; }
  .row:last-child { border-bottom: none; }
  .row:hover { background: var(--teal-dim); }
  .row:hover .arrow { color: var(--teal); }
  .label { font-family: var(--mono); font-size: 0.7rem; text-transform: uppercase; letter-spacing: 0.08em; color: var(--muted); }
  .value { font-size: 0.9rem; color: var(--text); }
  .arrow { font-size: 1rem; color: var(--muted); transition: color 0.15s; }
</style>
