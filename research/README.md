# Research Source Folder

The Research Agent's home. This is where raw data lives — mp4s, JSON scrapes, transcripts, press articles, screenshots. Everything the Analyst builds from starts here.

**Persistence Rule:** raw output goes to disk at its conventional path BEFORE any summarization, tagging, or Notion write. A Notion claim that doesn't trace to a path in this folder is not a claim.

---

## Layout

```
research/
├── heroes/          ← subjects of full Mode B hero studies (war room fodder)
│   ├── david-chang/
│   └── momofuku/
└── references/      ← bibliography / influences (Principles, Playbook, Production)
    ├── eyl/
    ├── kallaway/
    ├── oren-john/
    ├── alex-hormozi/
    ├── seth-godin/
    ├── donald-miller/
    ├── personal-brand-launch/
    └── acquired/
```

Each subject folder follows the same 4-layer structure:

```
<subject-slug>/
├── 00_subject.md       ← subject definition: handles, scope, time window
├── 01_raw/             ← untouched scraper output (per platform)
│   ├── instagram/
│   ├── youtube/
│   ├── tiktok/
│   ├── twitter/
│   ├── press/
│   ├── serp/
│   ├── backlinks/
│   ├── website/
│   ├── products/
│   └── services/
├── 02_tagged/          ← normalized JSON with auto-tags applied
├── 03_marked/          ← subset elevated for deep work
└── 04_deep/            ← Whisper transcripts, ffmpeg shot lists, full-text articles
    └── records/        ← per-asset Research Records (.md)
```

---

## Heroes vs References

**Heroes** are subjects of full Mode B hero studies. The Analyst Agent builds a war room from their data — Timeline, Character Map, Claim Bank, Segment Packets. The Scripting Agent pulls from that war room to write content.

**References** are the bibliography YUNG steals from. They feed the Principles, Playbook, and Production layers in Notion's References & Influences section. The same 4-layer storage layout applies so raw data is auditable, but the output destination is different (Principles/Playbook pages, not war rooms).

---

## Adding a new creator

1. Add an entry to `creators.json` at the repo root
2. Create the subject folder: `mkdir -p research/<heroes|references>/<slug>/{01_raw/{instagram,youtube,tiktok,twitter,press,serp,backlinks,website,products,services},02_tagged,03_marked,04_deep/records}`
3. Write `research/<heroes|references>/<slug>/00_subject.md` — handles, scope, time window, what you're trying to learn
4. Run the Research Agent

---

## File naming conventions

- Scraper output JSON: `01_raw/<platform>/<actor-slug>_<YYYY-MM-DD>.json`
- Asset files: keyed by platform native ID (shortCode for IG, video ID for YouTube, etc.)
- Run logs: `01_raw/<platform>/runs.log`
- Research Records: `04_deep/records/<platform>_<native-id>.md`
