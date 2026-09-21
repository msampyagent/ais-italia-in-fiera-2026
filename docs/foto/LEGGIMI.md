# Cartella foto

## Come caricare le foto

Metti qui i file delle foto rinominati con un numero progressivo a 3 cifre,
partendo da `001`:

```
docs/foto/001.jpg
docs/foto/002.jpg
docs/foto/003.png
docs/foto/004.webp
...
```

Estensioni accettate: `.jpg`, `.jpeg`, `.png`, `.webp` (anche miste).

Il sito prova a caricarle in ordine e si ferma quando trova 6 numeri
consecutivi mancanti. Tetto massimo: **140 foto**. Quindi **non lasciare
buchi** nella numerazione (001, 002, 003… senza saltare numeri).

## Podio (le prime in galleria)

Il podio si decide a mano in `podio.json`. È un array; ogni voce ha:

- `posicion` — numero intero. Vengono mostrate dalla minore alla maggiore.
- `foto` — percorso relativo alla root del sito (es. `foto/007.jpg`).

Esempio:

```json
[
  { "posicion": 1, "foto": "foto/012.jpg" },
  { "posicion": 2, "foto": "foto/003.jpg" },
  { "posicion": 3, "foto": "foto/041.png" }
]
```

Il numero di voci è libero: 3, 5, 10 — quante ne vuoi. Le foto del podio
vengono tolte dalla griglia sotto, che mostra tutte le altre in ordine
numerico di file.

Se `podio.json` è vuoto (`[]`) la pagina mostra solo la griglia.
