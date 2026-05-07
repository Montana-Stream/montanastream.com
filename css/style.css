/* ============================================
   Montana Stream — Wireframe / Clip-art style
   ============================================ */

:root {
  --bg: #f5f1e8;          /* warm paper */
  --ink: #1a1a1a;         /* line ink */
  --ink-soft: #2a2a2a;
  --accent: #2a2a2a;
  --header-h: 64px;
  --font-display: 'Georgia', 'Times New Roman', serif;
  --font-body: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}

* { box-sizing: border-box; margin: 0; padding: 0; }

html, body {
  height: 100%;
  background: var(--bg);
  color: var(--ink);
  font-family: var(--font-body);
  -webkit-font-smoothing: antialiased;
}

body {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

a { color: inherit; text-decoration: none; }

/* ============================================
   Header
   ============================================ */
.site-header {
  position: sticky;
  top: 0;
  z-index: 100;
  background: var(--bg);
  border-bottom: 1.5px solid var(--ink);
  height: var(--header-h);
}

.header-inner {
  max-width: 1300px;
  height: 100%;
  margin: 0 auto;
  padding: 0 24px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 24px;
}

.logo {
  display: flex;
  align-items: center;
  gap: 10px;
  font-family: var(--font-display);
  font-size: 1.15rem;
  letter-spacing: 0.02em;
  color: var(--ink);
}

.logo svg { display: block; }

.nav {
  display: flex;
  gap: 32px;
}

.nav a {
  position: relative;
  font-size: 0.95rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  padding: 6px 0;
  color: var(--ink);
  transition: opacity 0.2s ease;
}

.nav a::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 1px;
  background: var(--ink);
  transform: scaleX(0);
  transform-origin: right;
  transition: transform 0.3s ease;
}

.nav a:hover::after,
.nav a.active::after {
  transform: scaleX(1);
  transform-origin: left;
}

.nav-toggle {
  display: none;
  background: transparent;
  border: 1.5px solid var(--ink);
  width: 40px;
  height: 40px;
  cursor: pointer;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 4px;
  padding: 0;
}

.nav-toggle span {
  display: block;
  width: 18px;
  height: 1.5px;
  background: var(--ink);
}

/* ============================================
   Hero / Scene
   ============================================ */
.hero {
  position: relative;
  flex: 1;
  width: 100%;
  overflow: hidden;
  /* fill remaining viewport between header & footer */
  min-height: calc(100vh - var(--header-h) - 80px);
}

.scene {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  color: var(--ink);
  display: block;
}

.scene .mountains-back { opacity: 0.35; }
.scene .mountains-mid  { opacity: 0.6; }
.scene .pines          { opacity: 0.85; }
.scene .pines-front    { opacity: 1; }

/* ============================================
   Coming Soon — always centered
   ============================================ */
.coming-soon {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  z-index: 2;
  padding: 28px 48px;
  background: rgba(245, 241, 232, 0.85);
  border: 1.5px solid var(--ink);
  backdrop-filter: blur(2px);
  -webkit-backdrop-filter: blur(2px);
  max-width: 90vw;
}

.coming-soon h1 {
  font-family: var(--font-display);
  font-size: clamp(2rem, 6vw, 4.5rem);
  font-weight: 400;
  letter-spacing: 0.02em;
  line-height: 1.1;
  color: var(--ink);
}

.coming-soon .tagline {
  margin-top: 12px;
  font-size: clamp(0.85rem, 1.5vw, 1rem);
  letter-spacing: 0.3em;
  text-transform: uppercase;
  opacity: 0.7;
}

/* ============================================
   Footer
   ============================================ */
.site-footer {
  border-top: 1.5px solid var(--ink);
  background: var(--bg);
  padding: 20px 0;
}

.footer-inner {
  max-width: 1300px;
  margin: 0 auto;
  padding: 0 24px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
  flex-wrap: wrap;
}

.copyright {
  font-size: 0.9rem;
  letter-spacing: 0.05em;
  color: var(--ink);
}

.socials {
  display: flex;
  gap: 14px;
  list-style: none;
}

.socials a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 36px;
  height: 36px;
  border: 1.5px solid var(--ink);
  border-radius: 50%;
  color: var(--ink);
  transition: background 0.2s ease, color 0.2s ease;
}

.socials a:hover {
  background: var(--ink);
  color: var(--bg);
}

.socials svg {
  width: 18px;
  height: 18px;
  display: block;
}

/* ============================================
   Inner page content (videos/affiliates/about)
   ============================================ */
.page {
  flex: 1;
  max-width: 900px;
  margin: 0 auto;
  padding: 60px 24px;
  width: 100%;
}

.page h1 {
  font-family: var(--font-display);
  font-size: clamp(2rem, 4vw, 3rem);
  font-weight: 400;
  margin-bottom: 24px;
  border-bottom: 1.5px solid var(--ink);
  padding-bottom: 16px;
}

.page p {
  font-size: 1.05rem;
  line-height: 1.7;
  margin-bottom: 18px;
  opacity: 0.85;
}

/* ============================================
   Mobile
   ============================================ */
@media (max-width: 720px) {
  .nav-toggle { display: flex; }

  .nav {
    position: absolute;
    top: var(--header-h);
    left: 0;
    right: 0;
    background: var(--bg);
    border-bottom: 1.5px solid var(--ink);
    flex-direction: column;
    gap: 0;
    padding: 0;
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease;
  }

  .nav.open {
    max-height: 300px;
  }

  .nav a {
    padding: 16px 24px;
    border-top: 1px solid rgba(0,0,0,0.1);
    width: 100%;
  }

  .nav a::after { display: none; }

  .coming-soon {
    padding: 20px 28px;
  }

  .footer-inner {
    flex-direction: column;
    text-align: center;
  }
}
