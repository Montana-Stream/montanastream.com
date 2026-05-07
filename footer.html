/* ============================================
   Montana Stream — Header/Footer Injector
   Loads partials into any page that has
   #site-header and #site-footer divs.
   ============================================ */

(function () {
  // Helper: figure out the relative path to the partials/ folder
  // so this works whether a page is at root (/index.html) or
  // inside /pages/about.html, etc. Also works on GitHub Pages.
  function getBasePath() {
    const path = window.location.pathname;
    // Count how deep we are relative to the repo root.
    // If the page lives in a subfolder like /pages/, we need '../'.
    // We detect this by looking for known subfolders.
    const segments = path.split('/').filter(Boolean);
    // Last segment is the file (e.g. "about.html") or empty for "/"
    const lastIsFile = /\.html?$/i.test(segments[segments.length - 1] || '');
    const folderDepth = lastIsFile ? segments.length - 1 : segments.length;

    // Try to detect if we're inside a 'pages' folder
    if (segments.includes('pages')) {
      return '../';
    }
    return '';
  }

  async function injectPartial(targetId, file) {
    const target = document.getElementById(targetId);
    if (!target) return;

    const base = getBasePath();
    const url = base + 'partials/' + file;

    try {
      const res = await fetch(url);
      if (!res.ok) throw new Error('Failed to load ' + url);
      const html = await res.text();
      target.innerHTML = html;
    } catch (err) {
      console.warn('[Montana Stream] Could not load partial:', file, err);
    }
  }

  function highlightActiveNav() {
    const path = window.location.pathname;
    const file = path.split('/').pop().toLowerCase();
    const links = document.querySelectorAll('.nav a[data-page]');
    links.forEach((a) => {
      const page = a.getAttribute('data-page');
      if (file.includes(page)) {
        a.classList.add('active');
      }
    });
  }

  function setupMobileToggle() {
    const toggle = document.querySelector('.nav-toggle');
    const nav = document.querySelector('.nav');
    if (!toggle || !nav) return;

    toggle.addEventListener('click', () => {
      const isOpen = nav.classList.toggle('open');
      toggle.setAttribute('aria-expanded', String(isOpen));
    });
  }

  // Fix relative links inside partials when loaded into a subfolder page.
  // E.g. partial says href="videos.html" but page is in /pages/, so we
  // need to leave it as-is (since pages and partials live alongside).
  function fixHeaderLinks() {
    const base = getBasePath();
    if (!base) return; // we're at root, no fix needed

    const links = document.querySelectorAll('#site-header a[href]');
    links.forEach((a) => {
      const href = a.getAttribute('href');
      // Skip absolute URLs and anchors
      if (/^(https?:|#|\/)/i.test(href)) return;
      // If href is "index.html", point to root index
      if (href === 'index.html') {
        a.setAttribute('href', base + 'index.html');
      }
      // Otherwise (videos.html, about.html, affiliates.html) the file
      // sits in the same folder as the current page, so leave it.
    });
  }

  document.addEventListener('DOMContentLoaded', async () => {
    await Promise.all([
      injectPartial('site-header', 'header.html'),
      injectPartial('site-footer', 'footer.html')
    ]);
    fixHeaderLinks();
    highlightActiveNav();
    setupMobileToggle();
  });
})();
