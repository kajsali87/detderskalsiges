# Logoer til presse-striben

Bruges af `.press-logos` i `index.html` (hero-sektionen).

## Sådan virker farverne

Filerne indsættes **ikke** som `<img>`, men som CSS-maske:

```css
.press-logo{
  background-color: currentColor;          /* farven kommer herfra */
  mask: var(--src) no-repeat center/contain;
}
```

Billedet bruges altså kun som silhuet (alfa-kanal) — dets egne farver er
uden betydning. Derfor giver **én fil** både gråtone i light mode og lys i
dark mode. Farverne styres af `--logo` / `--logo-hi` i `:root` og i de to
dark mode-blokke øverst i `index.html`.

Konsekvensen er, at hvert logo bliver ensfarvet. Det er med vilje: en
presse-stribe skal læses som én række, ikke som seks konkurrerende
brand-farver.

## Filerne

| Fil | Mærke | Kilde | Licens |
|---|---|---|---|
| `berlingske.svg` | Berlingske (kun navnetrækket) | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Berlingskelogo.svg) | Public domain (PD-textlogo) |
| `berlingske-med-vaaben.svg` | Berlingske med våbenskjold | samme fil, ubeskåret | Public domain (PD-textlogo) |
| `jyllands-posten.svg` | Jyllands-Posten | jyllands-posten.dk (`#logo-jp`, deres eget masthead-mærke) | Varemærke, brugt som reference |
| `ekstra-bladet.svg` | Ekstra Bladet | [ekstrabladet.dk](https://ekstrabladet.dk/assets/svg/ekstrabladet.svg) | Varemærke, brugt som reference |
| `kontrast.png` | Kontrast | kontrast.dk (deres primære logo) | Varemærke, brugt som reference |
| `huffpost.svg` | HuffPost | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:HuffPost.svg) | Public domain (PD-textlogo) |
| `substack.svg` | Substack | [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Substack_logo.svg) | Public domain (PD-textlogo) |

Alle filer er efterbehandlet: metadata og editor-rester fjernet, faste
farver erstattet af `currentColor`, og `viewBox` strammet ind til det
faktiske motiv, så `--ar` i CSS'en passer.

### Berlingske: med eller uden våbenskjold

Standard er navnetrækket alene. Våbenskjoldet består af 64 separate paths
(93 KB mod 5 KB) og bliver en udtværet klat ved 16 px. Skal det med —
f.eks. hvis logoet skal vises større — skift stien i `index.html`:

```css
.press-logo.is-berlingske{
  --src:url(assets/logos/berlingske-med-vaaben.svg);
  --ar:5.581;   /* husk at rette --ar med */
}
```

### Ekstra Bladet

EB's mærke er et skjold med teksten banket ud i hvid. I masken er skjold og
tekst lagt sammen til én path med `fill-rule="evenodd"`, så bogstaverne
bliver rigtige huller. Derfor får de sidens baggrundsfarve i begge temaer —
præcis som i det ægte logo.

## Hvis et logo skal skiftes ud

1. Læg den nye fil her.
2. Ret `--src` under `.press-logo.is-<navn>` i `index.html`.
3. Ret `--ar` til filens bredde ÷ højde (brug dens `viewBox`, eller
   pixelmålene for en PNG). Ellers bliver logoet strukket.
4. Juster `--h` så mærket vejer optisk som naboerne.

PNG'er skal have gennemsigtig baggrund — masken bruger alfa-kanalen, så et
logo på massiv baggrund bliver til en firkant.
