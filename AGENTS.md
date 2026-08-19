# AGENTS.md — Det der skal siges

Instruktioner til AI-agenter, der arbejder i dette repo. Læs også [`README.md`](README.md) (opsætning) og [`ROADMAP.md`](ROADMAP.md) (strategi + åbne opgaver).

## Hvad det er

Personlig hjemmeside for **Kajsa Li Paludan** — skribent, essayist og foredragsholder. Publikationen "Det der skal siges" (Substack). Rolig, dannet, borgerlig/konservativ stemme: "argumenter, ikke vrede". Sproget er **dansk**.

- **Live:** https://kajsali87.github.io/detderskalsiges/
- **Repo:** `kajsali87/detderskalsiges` (GitHub Pages fra `main`, root)

## Filer

- `index.html` — HELE siden i én selvstændig fil. Alle billeder OG skrifter er indlejret som `data:`-URI'er (ingen eksterne afhængigheder; CSP-sikkert; virker offline/overalt).
- `assets/` — de behandlede billedkilder (sort/hvide, beskårne), som blev embeddet. Til genbrug/genbeskæring.
- `README.md`, `ROADMAP.md`, `AGENTS.md`, `CLAUDE.md`.

## Ufravigelige regler

1. **Ingen em-dashes (—).** Brug dansk tankestreg (–) med mellemrum, eller omskriv. Scan altid output for "—" før commit.
2. **Bevar det rolige, redaktionelle udtryk.** Løs teksttyngde med struktur (folde-ud, kort, luft, billeder) — ALDRIG ved at forsimple designet mod plain/sans/sort-på-hvidt.
3. **Hold `index.html` selvstændig.** Nye billeder/skrifter embeddes som data-URI'er; link ikke til eksterne filer.
4. **Verificér før du melder færdig.** Sig kun at noget virker, når det er tjekket.

## Design

- Titel: **Oswald** (kondenseret), med sidste ord "siges" i **Palatino**-serif kursiv, oxblood.
- Brødtekst: **Palatino**. Labels/menu: system-sans (versaler, letterspacing).
- Palet: bone `#F2F1EB`, blæk `#1B1A1E`, oxblood-accent `#7C2B2F` (sparsomt). Fuldt mørkt tema (accent lysnes til ca. `#D07A70` i dark).
- Fine hårstreger, meget luft, diskret scroll-reveal, sticky nav, burger-menu på mobil (venstre).
- Skrifter (Oswald + Bodoni Moda) er `@font-face` data-URI'er i toppen af filen.

## Sektionsrækkefølge

Hero → Tre indgange → Citat → Essays → Foredrag → Om → Bøger → Samarbejde → Book → Støt → Nyhedsbrev → Footer.

## Sådan tilføjer/behandler du et billede

1. Original ligger typisk i `~/Downloads` (Kajsa sender ofte billeder i chat — de kan IKKE trækkes ud som fil; find dem på disk, ofte som nyeste fil, eller bed hende gemme dem).
2. Behandl med Pillow: nedskalér (≈1300–1500 px bred), og for scene-/portrætbilleder som regel **sort/hvid** (`ImageOps.grayscale`) for at matche paletten. Beskær bevidst (hoved + hænder med).
3. Embed som `data:image/jpeg;base64,...`. Læg den behandlede fil i `assets/`.

## Deploy

Rediger `index.html` → commit → push. GitHub Pages bygger ~1 min. Afslut commit-beskeder med:

    Co-Authored-By: Claude Opus 4.8 <noreply@anthropic.com>

## Bloker / spørg først

Booking-mail, MobilePay-nummer, betalt Substack, presse-attributioner og CV-datoer er hendes egne data — bekræft ved tvivl (se ROADMAP "Åbne beslutninger").
