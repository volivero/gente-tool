# Where does conflict go? — GENTE decision tool and workshop materials

Interactive, single-file decision-support tool and facilitation materials for the workshop
**Engineering Governance for Just Energy Transitions: Integrated Methodologies for Multi-Stakeholder
Decision-Making** (WS 4), DAAD Global Centres Symposium 2026, Berlin, 1 October 2026, 13:30–15:30.

The tool lets a small group weight siting criteria with the Best–Worst Method, then move conflict and
governance between four positions in a spatial multi-criteria model — interpretive layer, weighted
criteria, veto threshold, sequencing tiers — and watch a departmental map of Colombia respond.
It runs from a single HTML file, with no server, no external libraries and no internet connection.

**Live copy:** `index.html` (v19). Open it in any browser, or download it for offline use from the link
in its footer.

## Repository layout

| Path | Contents |
|---|---|
| `index.html` | The tool, current version (identical to `tool/gente-decision-tool-v19.html`) |
| `tool/` | Versioned tool file, changelog, and source assets (boundaries, relief, font, logos) |
| `session/` | Facilitation script v2.0, handover brief, addendum and status notes (Spanish, internal) |
| `paper-kit/` | Paper backup: table sheets (EN), facilitator guide (ES), printable map plates (A3/A2) |
| `demo/` | Screen recordings of the tool and of a simulated participant run |
| `docs/` | Method notes and the final session abstract |

## Method and data

- Suitability results (viable area by department, onshore wind and utility-scale solar), the National
  Conflict Index and the National Governance Index come from the **GENTE project** (Gobernanza
  ENergética y TErritorio), developed by Universidad del Magdalena for the Agencia Nacional de
  Hidrocarburos (ANH) under **Contract 618 of 2025**. Onshore wind results are published in
  Olivero-Ortiz et al. (2026), *Land* 15, 923, CC BY (doi:10.3390/land15060923).
- Criteria weights use the Best–Worst Method (Rezaei 2015); consistency uses the input-based ratio and
  thresholds of Liang, Brunelli & Rezaei (2020), *Omega* 96, 102175.
- Department boundaries: Natural Earth (public domain). Shaded relief: Natural Earth / ETOPO1 (public
  domain). Typeface: Source Sans 3 (SIL Open Font License; see `tool/source/OFL.txt`).
- The tool operates at departmental scale because the two indices exist only at that level. The weights a
  table sets are recorded and compared with the expert panel but do not recompute the ranking, since
  per-criterion departmental scores are not available; the ranking responds to where conflict and
  governance are placed. This is stated in the tool's method section.

## What is deliberately not here

- The utility-scale solar manuscript, which is under review, and any material from it.
- GENTE deliverables (ANH property) beyond the figures already published or reproduced in the tool.
- Any participant list or correspondence with the organisers.
- The DAAD logo. The session takes place at a DAAD event but this is not a DAAD product.

## Publishing

The repository is ready for GitHub Pages: enable Pages on the main branch and `index.html` is served at
the root. A custom domain is set in the Pages settings plus the DNS records GitHub indicates. Tag the
frozen version (planned 21 September 2026) and mint a DOI for it on Zenodo.

## Attribution

Any derived product must attribute the GENTE project, developed by Universidad del Magdalena for the
Agencia Nacional de Hidrocarburos under Contract 618 of 2025. Session convened by the TRAJECTS Latin
America Hub. Chair: Víctor José Olivero Ortiz. Co-Chair: Andrea Cardoso.
