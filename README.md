# PerfScale Postmortems

Public incident postmortems for the PerfScale platform (perfscale.ru).

## Layout

- `template.mdx` — the template every postmortem starts from (frontmatter +
  required sections).
- `en/YYYY-MM-DD-<slug>.mdx` — English version.
- `ru/YYYY-MM-DD-<slug>.mdx` — Russian version.

Every postmortem is published in **both** languages; `<slug>` and the date
must match across locales so the site can pair them.

These files are rendered on <https://perfscale.ru/postmortems> — the site
consumes this repository as a git submodule.

## Writing a new postmortem

1. Copy `template.mdx` to `en/` and `ru/` with the incident date and a
   descriptive slug.
2. Fill in the frontmatter (`severity`, `status`, `incident_start`,
   `incident_end`, `downtime_duration`, `affected_services`).
3. Write the body: Summary, Impact, Root Cause, Timeline, Resolution,
   Follow-up Actions, Lessons Learned.
4. Keep `status: "draft"` until reviewed; flip to `"published"` afterwards.
   When the incident is fully closed (follow-ups tracked, fix verified in
   prod), set `status: "resolved"` — the postmortem stays on the site with a
   resolved marker.
