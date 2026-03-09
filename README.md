# Thomas Schulze IT Solutions

Personal portfolio and contact site for **Thomas Schulze – IT Solutions**, published via [GitHub Pages](https://pages.github.com/) with a custom domain.

**Live URL:** <https://thomas-schulze-it-solutions.de>

---

## Project overview

A zero-dependency, framework-free static website consisting of six pages:

| Page | File | Purpose |
|------|------|---------|
| Landing | `index.html` | Hero section, value-proposition cards, tech-stack chips |
| About | `about.html` | Bio, skills grid, experience stats, service list |
| Projects | `projects.html` | Project cards with tags and GitHub links |
| Contact | `contact.html` | Contact info + mailto: contact form |
| Impressum | `impressum.html` | Legal notice (required by German law) |
| Datenschutz | `datenschutz.html` | Privacy policy / Datenschutzerklärung (required by DSGVO) |

All pages share a single stylesheet (`css/style.css`) and two scripts (`js/i18n.js` and `js/main.js`).  
The site supports **German and English** (language switcher in the footer) and a **dark / light colour theme** (theme toggle in the footer).

---

## Local development

```bash
# From the repository root
python3 -m http.server 3000
```

Open <http://localhost:3000> in your browser.

Alternatively, use `npx serve .` or the [VS Code Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension.

---

## Testing

The site has a **Playwright** test suite in the `tests/` directory. Tests run against a locally served copy of the site and **never** touch the live site.

```bash
cd tests
npm install                                   # first time only
npx playwright install --with-deps chromium   # first time only

npx playwright test                           # run all tests
npx playwright test --headed                  # run with a visible browser
npx playwright test e2e/projects.spec.js      # run a single spec
```

CI runs the full suite automatically on every pull request to `main` via `.github/workflows/tests.yml`.

---

## Deployment

Push changes to `main` — GitHub Pages rebuilds and publishes the site within ~1 minute.  
The custom domain is configured in the repository settings; the live site is at <https://thomas-schulze-it-solutions.de>.

> Tests are a PR-gate only. Deploying does not trigger the test workflow, and test failures do not block deployment.

---

## Further documentation

Detailed developer documentation (architecture decisions, CSS conventions, JavaScript conventions, i18n guide, project data schema, design token reference, and more) is maintained in the [GitHub Wiki](https://github.com/thoooschuuu/thoooschuuu.github.io/wiki).
