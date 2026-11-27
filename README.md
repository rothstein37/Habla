# Habla · v1.3.0

Spanish practice web app, Hebrew-first, with offline-capable built-in content. A0 means pre-A1, not a formal CEFR level.

## Changes
- Local roster: choose an existing profile by stable ID; create and rename profiles in a separate management screen. Renaming preserves progress and scores. This is not authenticated administration, and local profiles/leaderboard are still per browser/device. No credentials, personal data or API keys in the public repository.
- 36 vocabulary packs, nine per level, five words each. Learn the words with meanings, examples and optional speech; practice only the current pack with multiple choice, listening, production, contextual completion and pictograms where suitable. Each word must be attempted before explicitly confirming readiness for the next pack. Pack position is stored per profile and level.
- 3874 structured question variants across all levels and packs (plus generated numbers). The original bank retains 3,034 items, with its old vocabulary questions replaced by pack-based variants during practice. Only the current pack is active.
- Local Spanish-to-Hebrew glossary with 1,080 mapped entries plus simple plural fallback. Hover or touch a displayed Spanish word. No external translation request; unknown words are labeled, not fabricated. Translations can depend on context.
- Exact accepted answers get full credit. Other open answers use approximate 0–10 word-overlap scoring against the best matching model, with negation warning and explanations. This is not a grammatical or semantic evaluation. Free responses can be valid despite low overlap; estimated points are not counted as verified correctness.
- Timed 5/15/30-minute automatic lessons; focused practice has no countdown. Home and Practice are distinct.
- Study time: visible exercise time with periodic local saving, excluding background and idle time after three minutes without input; today, today plus preceding six calendar days, and all-time. Legacy saved sessions are migrated once. Not a measurement of attention; older unrecorded time cannot be recovered.
- Same local-storage key as v1.2. No reset of existing profiles.
- Updated offline cache/version. Speech recognition uses browser services; physical-device compatibility and offline installation must be checked.

## Validation
JavaScript parsed. Mock DOM and storage tests checked normalized duplicate names, rename without loss, 36 packs and all choice variants, no premature advancement, exact and partial scoring, timed versus untimed practice, migration without double-counting, active/background/resumed study time, and seven-day cutoff. Static audit found local glossary entries or fallback for each Spanish word token in built-in questions and vocabulary examples. These are simulated and structural checks, not independent language review or live browser acceptance testing.

## Publish
GitHub Pages: Settings → Pages → Deploy from a branch → main / (root). Reload the published HTTPS site after deployment. No additional signup needed for local features.
For secure admin-issued accounts and shared cross-device scores, add an authenticated backend with server-enforced permissions. No backend service has been configured.
