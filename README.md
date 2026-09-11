# site-docs

Publicly served documents, published by GitHub Pages at
<https://wacaldwell.github.io/site-docs/>.

Public because some of these need publicly reachable URLs — Discord application
settings, for instance, require them for privacy policy and terms of service.

Policy text only. No code, no configuration, no data.

## Layout

One directory per subject, so documents for different things do not collide:

    counselor/    privacy policy + terms of service for the counselor Discord bot

## Source of truth

`counselor/` mirrors `docs/legal/` in the private counselor repository. Edit
there, then copy here, so the published text never drifts from the text the
project maintains.

## Workflow

Edit, commit to `main`, push. Pages rebuilds automatically. Check the live pages
afterwards — a Jekyll build failure is reported by email, not on the site, which
keeps serving the previous version.
