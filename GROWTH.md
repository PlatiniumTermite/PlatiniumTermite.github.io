# Flow — Growth System

Baseline (measured 2026-10-22): **78 total release downloads** across all
versions; v0.6.9 ≈ 10. No analytics, no Search Console history yet — these
numbers are the before-picture.

## Keyword opportunity matrix

Prioritized by relevance × attainable rank × conversion intent. No volume
claims — these need Search Console data to validate.

| Query cluster | Intent | Page that answers it | Priority |
|---|---|---|---|
| airdrop for windows / airdrop alternative | High — direct substitute | `/` + `/alternatives/airdrop/` | 1 |
| localsend alternative | High — competitor-curious | `/alternatives/localsend/` | 1 |
| share files mac windows / transfer files between mac and windows | High — exact use case | `/use-cases/mac-to-windows/` | 1 |
| send files android to pc / android to windows | High — exact use case | `/use-cases/android-to-windows/` | 1 |
| cross-platform file sharing | Medium — broad | `/use-cases/cross-platform-file-sharing/` | 2 |
| sync clipboard windows mac android | Medium — feature search | `/` FAQ + `/how-it-works/` | 2 |
| use another computer as second display / extended display wifi | Medium — feature search | `/` FAQ + `/how-it-works/` | 2 |
| kde connect alternative / quick share alternative | Medium — competitor-curious | comparison pages (expand later) | 3 |
| universal control alternative windows | Lower volume, high intent | `/use-cases/mac-to-windows/` | 3 |
| "is there airdrop for android" | Question format | FAQ schema | 3 |

**Rule kept:** every page answers a real question with original content — no
thin doorway pages.

## Measurement plan

What we can measure **today** without new infrastructure:

- **Downloads** — GitHub API `download_count` per asset (the only hard number).
  Baseline: 78 total, ~10 on v0.6.9.
- **Impressions & clicks** — Google Search Console (verification meta tag is
  live on every page; owner must click Verify, then submit `sitemap.xml`).
- **Bing** — submit same sitemap at bing.com/webmasters after GSC.

What's **not yet measurable** and needs a decision:

- Install activation, first transfer, 7-day retention — requires in-app
  telemetry, which conflicts with the privacy-first positioning. Option:
  privacy-respecting aggregate events (GoatCounter/Plausible on the site only,
  not the app) once an account exists.
- The honest stance: measure acquisition (site + downloads), not usage.

## Launch drafts — for review, NOT posted

### Product Hunt (draft)

- **Tagline:** AirDrop-style continuity for Windows, Mac & Android
- **Description:** Flow puts your devices in one space — they discover each
  other on Wi-Fi like AirDrop, pair with approval, and share files, folders,
  clipboard, screens, even a second display and keyboard/mouse link. Free,
  open, no accounts, nothing uploaded to a cloud.
- **First comment (maker):** what it is, why built, honest alpha status,
  roadmap (iOS app, signed builds), link to install.txt for warnings.

### Reddit (draft, adapt per subreddit rules)

- r/androidapps / r/windows / r/software angle: "I built an AirDrop-like app
  that works between Windows, Mac and Android — files, clipboard, screens.
  Open source, early alpha, would love brutal feedback." Lead with the
  honest-limitations list (unsigned builds, same-Wi-Fi, no iOS app yet) —
  Redditors reward candor and punish marketing.
- Do NOT cross-post the same text everywhere; one community at a time.

### Directories worth submitting

- AlternativeTo (list Flow as LocalSend/AirDrop alternative)
- Slant, StackShare, SaaSHub, opensourcealternative.to
- GitHub Awesome lists (awesome-selfhosted-adjacent file sharing lists)

## 30/60/90 roadmap

**Days 1–30 — indexing + proof**
- Verify Search Console, submit sitemap, confirm all 12 URLs indexed
- Submit Bing Webmaster Tools
- Post to 1–2 relevant communities (drafts above, adapted honestly)
- Track download_count weekly — first external-download evidence
- Ship signed macOS build (kills the #1 install objection)

**Days 31–60 — authority**
- Real product screenshots/screen-recording GIF on the homepage (real, from
  the shipped app — no mockups)
- Expand comparisons: KDE Connect, Quick Share — same honest format
- AlternativeTo + directory submissions
- First real-user feedback loop → fix top friction

**Days 61–90 — conversion depth**
- Privacy-conscious site analytics (once an account exists)
- iOS progress updates → waitlist-style interest capture if native ships
- Iterate titles/FAQ based on actual Search Console query data
- Physical-device demo video — the strongest conversion asset possible

## External actions needing YOU

1. **Search Console** — click Verify (meta tag already live), submit
   `sitemap.xml`
2. **Bing Webmaster** — bing.com/webmasters, same URL + sitemap
3. **Apple Developer cert** — still the only thing between alpha builds and
   warning-free macOS installs; CSR is ready at
   `~/.config/flow/signing/DeveloperID.certSigningRequest`
4. **Community posts** — drafts above; posting from a real human account is
   required and right (bots get banned)
5. **Analytics account** — pick GoatCounter (free, privacy-first) or
   Plausible; I'll wire the snippet once the account exists

## What's deliberately NOT done

- No fabricated ratings, testimonials, download counts or review schema
- No mass-produced thin keyword pages
- No paid backlinks, no comment spam, no review manipulation
- No in-app telemetry — privacy positioning is a feature
