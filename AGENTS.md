# AGENTS.md: Assignment 1, Accelerated Prototyping

## The idea
**Stoop**: a reimagined craigslist. A local classifieds board with no fees and no algorithm, covering one city's neighborhoods (for sale, free stuff, housing, jobs, gigs, services, community).

- **Who it's for:** people in a city who want to buy, sell, swap, or give things away nearby, or find a room or a gig, without the noise of big platforms. Covers both posters and browsers, at any level of tech comfort.
- **What a visitor should understand:** this is a plain, trustworthy, local board where you deal directly with your neighbors.
- **What a visitor should do:** browse a category or search, *or* post a listing in under a minute.

## Assignment goals
- 25 distinct landing pages (`/v01/` … `/v25/`) plus a gallery at `/index.html` that tells the story of the process and presents the final choice.
- v01–v10: go wide (radically different layout, era, mood, tone; changing only colors or fonts doesn't count).
- v11–v19: narrow down by combining what worked. v20–v25: converge and refine. v25 is the final.
- At least 20 designs must look unlike anyone else's in the class. Avoid generic SaaS/landing-page templates.

## Constraints
- Plain HTML + CSS, optional vanilla JS. No frameworks, packages, build step, external APIs, or data storage. No CDN fonts or images: use system fonts, inline SVG, and CSS only.
- Each version is self-contained in `vNN/index.html` and has a visible "← Gallery" link back to `/`.
- Listings are fake but plausible (realistic prices, neighborhoods, quirky local details).
- One commit per version so the history shows the iteration.
- Deploy: GitHub repo + Vercel Hobby (static, no config needed).
- Gallery notes for each version live in the `VERSIONS` array in `index.html`.

## Process log (update as we go)
- v01–v10: wide exploration round (see the gallery notes).
- **Round 1 review (user's decisions):**
  - Kept: the type of v02 and v07 (modern, bold, minimal), v06's map, and v07's recent-listings table.
  - Dropped: v01, v04 and v09 ("kitschy, not in a good way"), v09 also "too chaotic", and v10 ("doesn't make sense in this context"). v03, v05 and v08 weren't carried forward.
  - Search is the tentpole. It gets equal weight with "Post a listing" (search OR post).
  - Page order: search/post → recent listings → map.
  - Setting: Chicago neighborhoods.
- v11–v19: narrowing round. Each version tries a different layout and interaction for that same hierarchy and type direction.
- **Round 2 review (user's decisions):**
  - Out: v17 ("clever but unnecessary"), v13 and v11 (the vertical split screen is distracting/unattractive), v19 ("too similar to existing craigslist"), and v18 ("fun but not functional, looks like a data visualization"). v12's thick borders are distracting.
  - Liked: v12 and v14 are straightforward and take little effort.
  - Winner structure: v16's calm FIND/POST first screen (not overwhelming, direct), then scroll to v15's list + sticky map workspace.
  - Post needs more body: title + description + photo upload, not just a one-word title.
  - Palette: light blue, cream, white. No black/white scheme.
- v20–v25: converge. v20 = v16 hero + v15 workspace + rich post + new palette; later versions refine it.
- **v20 review (user's decisions):** "almost perfect, just minor tweaks." Drop the word "Age". Add log in/sign up so people can favorite listings and organize them. Grey out listings you've already viewed.
  - v21 "Posted" wording + viewed = grey · v22 log in/sign up dialog · v23 favorites · v24 collections to organize favorites · v25 final polish (mobile map scroll, consistency).
  - Sign-in, favorites and viewed state are in memory only (the no-storage rule).
