---
name: hjalp
description: Kör detta när något krånglar eller du inte vet vad du ska göra härnäst. Diagnostiserar och föreslår EN åtgärd på svenska.
---

# /hjalp — något krånglar, vi löser det tillsammans

Användaren bygger "Stämmoprotokollet", är nybörjare och kan inte felsöka själv. Var lugn och
trygg ("inga problem, det här fixar vi"). Visa ALDRIG en rå stacktrace — översätt allt till
vardagssvenska.

Kör diagnosen i ordning:
1. Läs `docs/FRAMSTEG.md` → vad var vi mitt i?
2. Kör `npm run build` (eller `npx tsc --noEmit`) → läs felet och översätt till EN mening på svenska.
3. Kolla `.env.local` → saknas nycklar som behövs (Supabase-URL/anon-key, ev. ANTHROPIC_API_KEY)?
4. Kör `node --version` → om < 18, be dem installera senaste LTS från nodejs.org.
5. Kör `git status` → något halvgjort som ställer till det?

Vanliga fel → åtgärd:
- "Cannot find module" → `npm install`.
- Saknad/fel `.env.local` → fyll i rätt nycklar (aldrig i koden).
- "relation ... does not exist" → tabellen saknas i Supabase, kör migrationen.
- Port upptagen → starta om dev-servern.
- Vercel build-timeout → höj `maxDuration` på routen.

Avsluta ALLTID så här:
- Säg i EN mening vad som var fel.
- Föreslå EN konkret åtgärd och fråga "ska jag fixa det?".
- Påminn: inget är trasigt för gott — du sparar hela tiden med `git commit`, och `/rewind` finns.
