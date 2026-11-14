# WordSprout: Public Demo

**WordSprout** is a web-based English tutoring platform for K-12 English Language Learners. I built it as a former EL teacher to address a need I saw in my own classroom, then piloted it with 3 students and used their feedback to refine it (for example, adding a phonics section to support reading fluency).

**This repository is a limited public demo.** It is *not* the full product.

## What you can try
Open the live demo and use the built-in sample student ("Sample Student"). A small sample of each learning area is included:

- Listening (dictation), Speaking (describe a picture), Reading, Writing
- Word Anatomy Studio (fix the sentence), Syllable Sprout, Phonics (Kindergarten to Grade 2)
- A sample Placement Screener result, badges, and the Learning Standards page

## What is intentionally *not* in the demo
- **No accounts, no database, no student data.** Progress lives only in your browser tab and resets when you refresh.
- **No AI calls.** "Ask Buddy" shows a canned message in the demo.
- **No payments, messaging, homework upload, assessments or admin tools.**
- **Only a sample of the lesson content.** The full lesson library, assessments and screener are not included.

## The full product (not published here)
| Layer | Technology |
|---|---|
| Front end | Plain HTML/CSS/JavaScript, hosted on GitHub Pages |
| Auth and database | Supabase (Auth, Postgres, Row-Level Security with least-privilege permissions) |
| Backend logic and secrets | Supabase Edge Functions (API keys never reach the browser) |
| AI tutor | Anthropic API (text) |
| Text-to-speech | ElevenLabs |
| Email | Resend |
| Reliability | Automated daily health checks with GitHub Actions |
| Built with | Claude as a coding assistant |

## Design decisions and trade-offs
- **Why a separate demo?** A browser app's front-end code is always visible to visitors, so protection has to come from the back end (database rules, server-side functions) and from limiting what is published. The demo therefore has no backend connection at all, which also means nothing can be abused or run up costs.
- **Student privacy first.** The full app is designed around student data protection. A formal COPPA/FERPA review and red-team testing of the AI features are planned before any wider use.
- **Pilot-driven.** Features were adjusted after real students used the app.

## License and use
Copyright (c) 2026 Willie D. Boone III. **All rights reserved.** This demo is provided for viewing and evaluation only. Copying, modifying, redistributing, or reusing the code or content without written permission is not allowed. See `LICENSE`.

Contact: WordSprout726@gmail.com
