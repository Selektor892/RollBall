# BallBall

Calcio 3D a sfere con visuale dall'alto, nel browser. Giocatori e palla sono sfere: spingi, tira, segna.

**Gioca:** apri `index.html` nel browser, oppure la versione online su GitHub Pages.

## Modalità
- Tu contro la CPU (3 livelli di difficoltà)
- 1 contro 1 sulla stessa tastiera
- 2 contro 2, ognuno con un compagno CPU
- Cooperativa: due giocatori contro due CPU

## Comandi
| | Muovi | Tira |
|---|---|---|
| Giocatore 1 (Rossi) | W A S D | Spazio |
| Giocatore 2 (Blu) | Frecce | Invio o Ctrl destro |
| Touch (telefono in orizzontale) | pollice sinistro, trascina | pollice destro, tieni premuto |

Esc o P pausa · V cambia visuale · M audio

Tieni premuto il tasto di tiro: l'anello bianco si accende e la palla parte appena la tocchi. Pareggio a fine tempo: golden goal.

## Tecnica
Un solo file HTML con [Three.js](https://threejs.org/) r149 caricato da CDN. Nessuna build.

## Opzioni nel menu
- **Durata**: 2, 3 o 5 minuti, oppure senza limite di tempo.
- **Gol per vincere**: libero, 3, 5, 7 o 10. La partita finisce appena una squadra ci arriva.
- **Visuale**: inclinata (3D) o dall'alto. Si cambia anche in partita con V o con il tasto 3D sul telefono.

## Schermo intero su telefono
Su Android il gioco va a schermo intero quando premi Gioca, e c'è un tasto apposito in alto a destra. Su iPhone Safari non permette lo schermo intero alle pagine web: usa Condividi → Aggiungi alla schermata Home e apri il gioco da lì.
