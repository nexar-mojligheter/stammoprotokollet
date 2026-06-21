# Stämmoprotokollet

> **STOPP — gör detta allra först:** kör skillen `/start`. Föreslå INGEN plan och ställ
> INGA tekniska frågor innan dess. `/start` leder användaren (som kan vara helt ny) steg
> för steg. **Du LEDER och fattar alla tekniska beslut själv** (logga i docs/BESLUT.md) —
> be aldrig användaren välja tech, integration eller betalning.
>
> Researchad möjlighet från Nexar Academy. Full marknadsresearch finns i skillen `/affarsplan`.

## Vad vi bygger
Generera juridiskt korrekta BRF-stämmoprotokoll på minuter – inte timmar.. Stämmoprotokollet är ett AI-drivet verktyg byggt specifikt för bostadsrättsföreningars årsstämmor och extra stämmor – med full hänsyn till bostadsrättslagens särkrav på kallelse, röstlängd och omröstningsregler. Slipp juridiska fallgropar och spara styrelsens värdefulla ideella tid. Klart, korrekt och klart att skriva under direkt efter mötet.

## Stack (ändra inte utan att fråga)
- Next.js + Tailwind (frontend)
- Supabase (databas + auth)
- Vercel (deploy)
- Claude API där appen behöver AI

## Kommandon
- `npm run dev` — kör lokalt
- `npm run build` — bygg + felkoll (kör efter varje ändring)
- `npm run lint` — lint

## Så jobbar vi (viktigt)
- **DU leder.** Användaren kan vara helt ny — håll dem i handen, ett steg i taget, förklara i vardagsspråk.
- **Ta tekniska beslut själv** (tech, datamodell, integrationer, betalning) med sunda standardval och logga dem i `docs/BESLUT.md`. Dumpa ALDRIG tekniska val på användaren.
- Fråga bara om sånt användaren faktiskt har en åsikt om — i vardagsspråk och med en tydlig rekommendation. Föreslå EN väg, inte en meny av alternativ.
- Bygg i **små steg** — kör `npm run build` efter varje ändring och visa resultatet.
- **Fira framsteg.** Efter varje klart steg: säg vinsten i klartext ("nu kör din app lokalt 🎉"), skriv den i `docs/FRAMSTEG.md`, och peka på nästa ENDA mikrosteg.
- **Allt går att ångra.** Säg det tidigt till användaren. Kör `git commit` INNAN något riskfyllt (deploy, databas-migration, större ändring) så inget kan förstöras permanent. `/rewind` finns som extra skyddsnät.
- Lägg **aldrig** hemligheter/nycklar i koden — bara i `.env.local`.
- Håll det **enkelt** — en MVP som bevisar värdet.

## Projektminne (DU ansvarar för det — användaren ska aldrig behöva be)
- Efter varje avklarat steg: uppdatera `docs/FRAMSTEG.md` (byggt + nästa steg).
- Vid varje vägval: logga en rad i `docs/BESLUT.md` (datum + 1 mening om varför).
- Bocka av i `docs/UPPGIFTER.md` allt eftersom.
- **Vid sessionsstart: läs `docs/FRAMSTEG.md` FÖRST** och sammanfatta "var vi var".
- Använd din inbyggda auto-memory för build-kommandon och buggfixar.

## När något går fel (viktigt för tryggheten)
Visa ALDRIG en rå stacktrace för användaren. Säg istället, på svenska:
1. Vad som hände (en mening, vardagsspråk).
2. Att det är vanligt och inte deras fel.
3. Vad du gör nu för att lösa det.
Vanliga fel → åtgärd: saknad `.env.local` → fyll i nycklarna · "Cannot find module" → `npm install` · fel Node-version → senaste LTS från nodejs.org · "relation does not exist" → tabell saknas, kör migrationen · Vercel-timeout → höj `maxDuration`. Krånglar något: kör `/hjalp`.

## Kom igång
**Kör `/start` — alltid, först av allt.** Den leder dig (och mig) steg för steg från noll till färdig app: frågar om din nivå, förklarar varje verktyg (Supabase, Vercel m.m.), hjälper dig installera, och bygger. Föreslå INTE en MVP-plan på egen hand — kör `/start`.

Skills att känna till: `/start` (kom igång), `/nasta-steg` (kom tillbaka en annan dag → "var var vi, vad är nästa steg"), `/hjalp` (något krånglar), `/rapportera` (appen blev live eller fick första kund), `/affarsplan` (marknadsresearchen).

<!-- nexar:opportunity slug=stammoprotokollet -->
