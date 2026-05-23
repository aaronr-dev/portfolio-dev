<script>
  import '../app.css';
  import { page } from '$app/stores';
  const links = [
    { href: '/',           label: 'Home' },
    { href: '/experience', label: 'Experience' },
    { href: '/projects',   label: 'Projects' },
    { href: '/contact',    label: 'Contact' },
  ];
</script>
<header>
  <nav>
    <a class="logo" href="/">AR</a>
    <ul>
      {#each links as link}
        <li><a href={link.href} class:active={$page.url.pathname === link.href}>{link.label}</a></li>
      {/each}
    </ul>
  </nav>
</header>
<main><slot /></main>
<footer>
  <span>Aaron Rodriguez · aaron@aaronr.dev</span>
  <div class="footer-links">
    <a href="https://linkedin.com/in/aaronjrodriguez" target="_blank" rel="noopener">LinkedIn</a>
    <a href="https://github.com/aaronr-dev" target="_blank" rel="noopener">GitHub</a>
  </div>
</footer>
<style>
  header { border-bottom: 1px solid rgba(255,255,255,0.08); position: sticky; top: 0; z-index: 100; background: var(--bg); }
  nav { max-width: var(--max-w); margin: 0 auto; padding: 0 2rem; height: 64px; display: flex; align-items: center; justify-content: space-between; }
  .logo { font-family: var(--mono); font-size: 1rem; color: var(--teal); font-weight: 500; letter-spacing: 0.1em; }
  ul { list-style: none; display: flex; gap: 0.25rem; }
  ul a { font-size: 0.85rem; color: var(--muted); padding: 0.45rem 1rem; border-radius: 6px; transition: color 0.15s, background 0.15s; }
  ul a:hover { color: var(--text); background: rgba(255,255,255,0.06); }
  ul a.active { color: var(--teal); background: rgba(20,184,166,0.1); }
  main { max-width: var(--max-w); margin: 0 auto; padding: 3.5rem 2rem; }
  footer { border-top: 1px solid rgba(255,255,255,0.08); max-width: var(--max-w); margin: 2rem auto 0; padding: 1.75rem 2rem; display: flex; justify-content: space-between; align-items: center; font-family: var(--mono); font-size: 0.72rem; color: var(--muted); }
  .footer-links { display: flex; gap: 1.5rem; }
  .footer-links a { color: var(--muted); transition: color 0.15s; }
  .footer-links a:hover { color: var(--teal); }
</style>
