# Media Ponderata

Web app (singolo file HTML, nessuna dipendenza) per calcolare la **media ponderata** con **analisi di sensitività per riga**.

## Funzioni

- 3 righe iniziali, 2 colonne (A e B); puoi aggiungere o eliminare righe.
- Ogni colonna può contenere **quantità** oppure **percentuali**.
- Scegli quale colonna fa da **peso**; l'altra è il **valore**.
- Risultato: media ponderata (in % se la colonna valore è in percentuale).
- Sensitività per ogni riga:
  - peso relativo sul totale;
  - contributo alla media;
  - Δ media se il valore della riga aumenta di 1 unità (o 1 punto percentuale);
  - Δ media se il peso della riga aumenta di 1 unità (o 1 punto percentuale).
- Installabile come app (PWA) e funzionante offline, con icona.

## Formula

```
M = Σ(wᵢ · vᵢ) / Σ wᵢ
∂M/∂vᵢ = wᵢ / Σw
ΔM per wᵢ → wᵢ + Δ  =  (S + vᵢ·Δ)/(W + Δ) − M
```

Se i pesi in percentuale non sommano 100%, la media viene normalizzata sulla somma dei pesi e compare un avviso.

## Pubblicare su GitHub Pages

1. Crea un repository e carica **il contenuto** di questa cartella nella radice (senza sottocartella).
2. Vai in *Settings → Pages*, scegli *Deploy from a branch*, branch `main`, cartella `/ (root)`.
3. Dopo qualche minuto l'app sarà su `https://<utente>.github.io/<repo>/`.

Da lì puoi usare "Aggiungi a schermata Home" su telefono o "Installa app" su desktop.
