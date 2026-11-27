# Habla · v1.2.0
Personal Spanish-learning web app. Preserves the v1.1 Hebrew-first interface and local storage key. A0 means pre-A1, not a formal CEFR certification. No paid services, personal data, API keys or login credentials are included.

## What's new
- 3034 built-in exercises: A2 1028, B1 1045, A1 605, A0 356. Includes original questions, controlled grammar and phrase variants, and open tasks; numbers are generated separately. Variants may revisit the same vocabulary or grammar skill. Stable IDs and local seen history prioritize unseen questions across sessions; repeats can occur when the selected pool is exhausted, on a fresh device, after storage loss, or after changing formats.
- 5 minutes: up to 2 skills in auto mode; 15: balanced rotation; 30: increased writing/speaking emphasis. Focused mode stays on the selected skill.
- A0 profile option and A0 number range 0–20. Removed JSON export and level-test references from visible settings; local progress is preserved when updating on the same origin.
- Speech recognition starts directly from a user click; handles unsupported APIs, insecure contexts, offline, permission, no-speech, audio capture and network errors. Transcript can be edited before assessment. Microphone and device support not guaranteed. No pronunciation scoring or free-response AI. Keyboard dictation/typing fallback. Browser transcription may send audio to a browser service.
- Responsive mobile web app, manifest, network-first navigation with cached offline fallback, version check on reconnect/foreground; new published content loads on online navigation. Update prompt does not interrupt an active lesson. After initial successful online caching, text exercises can work offline. Offline TTS needs a local voice; transcription requires compatible connected browser. Browser may clear local data.

## Publish
In GitHub: Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main / (root) → Save. Wait for deployment, then open the published HTTPS address shown by Pages. For Android use Chrome Add to Home screen / Install app where offered; on iOS use Safari Share → Add to Home Screen. First open online. Real device installation, microphone and offline behavior still need testing.

## Checks in this release
Both scripts and service worker parsed in JavaScript. Checked unique IDs, four distinct choices and valid correct answers for all multiple-choice items. Simulated DOM/storage tests selected 120 distinct questions per level and a fresh question in the next session, exercised durations, A0 numbers, feedback, removed settings, and mocked speech recognition including permission error. These are not physical-device tests; generated language content is not a certified curriculum and has not been independently reviewed item-by-item.

## Known limitations
Local profiles and leaderboard are per device/browser only; cross-device user accounts and a shared leaderboard need an authenticated backend (e.g. Supabase) with access control. No registration or expenditure has been initiated. Existing downloadable file previews use a different origin than Pages, so their browser data does not automatically transfer. No external AI feedback yet; unknown open answers receive a model and self-check rather than invented grade. Not designed for use while driving. Content is updated when new versions are committed/published; no autonomous AI content-generation service.
