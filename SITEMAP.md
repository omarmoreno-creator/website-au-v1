# Site Map — website-au-v1

Single-page React-style prototype (`index.html`) implementing client-side routing via a `route` state variable. All views are bundled in one file; navigation uses anchor links wired to `setRoute(...)`.

## Primary navigation (header)

| Label | Route id | Notes |
|---|---|---|
| (logo) | `home` | Brand → home |
| Programs | `programs` | Has mega-menu; also matches dynamic `program:<slug>` routes |
| Admissions | `admissions` | |
| Tuition | `tuition` | |
| Why Atlantis | `why` | |
| Study | `flex` | Format/modality selector |
| Careers | `careers` | Outcomes & employers |
| International | `international` | F-1, languages, countries, funding |
| Apply now (CTA) | `apply` | Multi-step application form |
| Search (icon) | `search` | |

Utility bar (top): Global campus · Student portal · Request info · EN · ES.

## Route map

```
home              → HomePage          (hero, featured programs, schools, news, visit)
programs          → ProgramsPage      (filterable program index + mega-menu source)
program:<slug>    → Program detail    (dynamic; one per program)
apply             → ApplyPage         (4-step wizard: About you → Program → Background → Review)
admissions        → AdmissionsPage    ("Four steps to Atlantean", requirements, deadlines)
tuition           → TuitionPage       (cost breakdown + three payment paths)
why               → WhyPage           (faculty, employers, alumni)
flex              → FlexPage          (campus selector + pace selector)
careers           → CareersPage       (where graduates land, top hirers)
international     → InternationalPage (SEVP, Language Institute, top countries, funding)
search            → search view
```

## Apply flow (route = `apply`)

Four sequential steps within the same route:
1. **About you** — basic contact info
2. **Choose your program** — program selector
3. **Academic background** — credentials
4. **Review & submit** — confirmation

## Key sections on Home (`route = home`)

- Hero
- Featured programs grid
- "Explore by school." (school cards)
- "Faculty who've done the work."
- "What's happening at Atlantis" (news)
- "Visit us"

## Assets

- `assets/hero-graduation.jpg`, `assets/hero-healthcare.jpg` — hero imagery
- `assets/logo_horizontal.webp`, `assets/logo_mark.webp` — branding
- `fonts/` — OpenSans (regular + italic) + Oswald variable fonts

## Notes

- All routing is in-memory; there are no separate HTML files per page.
- Program-detail pages use the `program:` route prefix with a slug suffix.
- A "Page under construction" placeholder exists as a fallback for unimplemented routes.
