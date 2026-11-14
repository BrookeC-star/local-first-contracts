# Local First Contracts

When a large data facility comes to a neighborhood, local companies and agencies should see lease and contract opportunities first, and everyone should be able to check who got the work.

Context: Quantum Shore Chicago (former U.S. Steel South Works site, South Side). The same problem applies around any large data facility.

## Files
| File | What it is |
|---|---|
| `index.html` | The prototype and site home page: opportunities list, eligibility check, bidding, transparency ledger. Open in a browser. |
| `slides.html` | 7-slide deck. Arrow keys to navigate, Ctrl+P to save as PDF. |
| `accountability-old.html` | Earlier prototype (community accountability dashboard). Kept for reference; not the current direction. |

## Run it
Open `index.html` in a browser. No build step, no dependencies.
For a public Working URL: push this folder to a GitHub repo, then Settings > Pages > Deploy from branch `main` / root.

## Concept framework
Publish (developer posts scopes in small lots) > Verify (business proves it is local) > Local-first window (verified local bidders go first, then open to all) > Award (winner and amount published) > Track (local share promised vs. actual, which sets the next target).

## Users and payer
- **Users (free):** local companies, community organizations and local agencies near the facility.
- **Payer (hypothesis):** the developer, per project, for posting, verification, local-first windows and compliance reports.
- **Governance (planned):** independent non-profit ownership; awards and local share are public; payment buys service, not outcomes.
- No developer has agreed to pay. Pricing and market size are untested.

## Tech framework and why
- Single-page HTML, CSS and plain JavaScript. No framework, no external libraries, no server.
- Hosted on GitHub Pages.
- Bids are stored in the browser's `localStorage`. Sample data is hard-coded.

Why: one hour of build time, no team framework experience, a free public URL is required, and a static page cannot crash during a live demo.

| | Pros | Cons |
|---|---|---|
| Development | Fast, simple, easy to debug | One file gets hard to maintain; no reusable components |
| Deployment | Free, live in minutes | Static only; no back end |
| Data | No server or security cost | Not shared between users; lost if browser data is cleared |
| Privacy | No real personal data collected in the demo | A real version must handle company and address data |
| Growth | Logic can be moved into a framework or back end later | Needs partial rewrite to scale |

## Known limitations and edge cases
Technical:
- ZIP code is self-entered, so anyone can claim to be local. Largest gap; the prototype has no identity or eligibility verification.
- Bids are per browser: duplicates are possible and records vanish in private mode or after clearing data.
- The local-first window is displayed as a number of days; there is no real countdown and no time zone handling.
- English only; no Spanish version and no screen-reader testing. Not tested across browsers or on mobile.

Product:
- "Local" is undefined in practice: a locally registered firm with non-local owners, or a branch of a chain.
- No local bids by the end of the window: it should open to all automatically (not implemented).
- Only one local bidder: direct award or still compare prices?
- Subcontracting to non-local firms after award is not visible in the ledger (only first-tier winners).
- Developer-entered award data may not be trusted; independent checking is needed.

## Data note
| Item | Status |
|---|---|
| Opportunities, company names, award amounts, 40% local target, local ZIP list | **Illustrative.** Invented for the mockup. Not real contracts or companies. |
| Virginia JLARC: about 1,500 peak construction workers, about 50 permanent staff per typical facility | From secondary sources (Data Center Knowledge, Lightcast). Verify the original study before citing. |
| iqmp.org FAQ: "hundreds" of jobs, no local-hire commitment, no investment or power figures | Our reading of the park's FAQ and chicagoquantum.org/IQMP. Absence on those pages only. |
| "$9B South Side project" | Chicago 312 newsletter headline. Not independently verified. |
| Competitors (Procore, BuildingConnected, government supplier-diversity programs) | From general knowledge, not researched. Verify before presenting. |
| Current Chicago/Illinois local-hire and certification rules | **Not researched.** Needed before claiming how this differs. |

## Next steps after the hackathon
- 1 to 2 weeks: interview local firms and community groups; research existing local-procurement and certification rules.
- 1 to 3 months: pilot with one developer on one scope; test willingness to pay.
- 3 to 6 months: apply for start-up grants; set up independent governance; add back end, eligibility verification and Spanish.

## Other known gaps
- No news found after late August 2026 about Quantum Shore (data center moratorium vote, Related Digital's north-end plan).
- Local organizations (e.g. Southside Together) were not consulted.
