# Det der skal siges — Kajsa Li Paludan

Hjemmeside for Kajsa Li Paludan, skribent og foredragsholder.

- **Live:** https://kajsali87.github.io/detderskalsiges/
- **Kilde:** [`index.html`](index.html) — én selvstændig fil. Alle billeder og skrifttyper er indlejret som data-URI'er, så siden virker overalt uden eksterne afhængigheder.
- **Billedkilder:** [`assets/`](assets/) — de behandlede (sort/hvide, beskårne) billeder, der bruges på siden. Nyttige, hvis noget skal genbeskæres.

## Sådan opdaterer du siden

1. Ret i `index.html`.
2. Kør:

   ```bash
   git add -A && git commit -m "kort beskrivelse" && git push
   ```

3. GitHub Pages bygger og opdaterer siden automatisk (~1 minut). Hård-genindlæs, hvis browseren viser den gamle version.

## Design

- **Titel:** Oswald (kondenseret) med det kursiverede "siges" i Palatino-serif.
- **Brødtekst:** Palatino. **Labels/menu:** system-sans.
- **Palet:** bone-papir `#F2F1EB`, blæk `#1B1A1E`, oxblood-accent `#7C2B2F`. Fuldt mørkt tema.
- **Skrifter** (Oswald + Bodoni Moda) er indbygget i filen som `@font-face` data-URI'er.

### Regler
- **Ingen em-dashes** (—). Brug dansk tankestreg (–).
- Maks. to linjer ad gangen i de "skarpe" afsnit; del gerne sætninger.
- Behold det rolige, redaktionelle udtryk — fiks teksttyngde med struktur (folde-ud, kort, luft), ikke ved at forsimple designet.

## Sektioner

Hero → Tre indgange → Citat → Essays → Foredrag → Om → Bøger → Samarbejde → Book → Støt → Nyhedsbrev → Footer.

## Endnu ikke på plads

- Booking-mail: `kontakt@kajsapaludan.dk` (bekræft/skift ved behov).
- MobilePay: svensk nummer indtil videre (skift til dansk for at undgå gebyr).
- Betalt Substack-abonnement er ikke slået til endnu ("Bliv støttemedlem").
- Facebook linker til profilen; X mangler et link.
- Evt. eget domæne (fx `kajsapaludan.dk`) kan kobles på GitHub Pages.
