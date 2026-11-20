# RollBall

Calcio 3D a sfere con visuale dall'alto, nel browser. Giocatori e palla sono sfere: spingi, tira, segna.

**Gioca online:** https://selektor892.github.io/RollBall/ (oppure apri `index.html` nel browser).

## Modalità
- **Online**: uno crea una stanza e riceve un codice di 4 caratteri, l'altro lo inserisce in "Entra in una stanza". Chi crea la stanza gioca con i Rossi e sceglie formato (1 contro 1 o 2 contro 2 con CPU), durata e gol per vincere.
- **Locale**: partita contro la CPU, 1 contro 1 sulla stessa tastiera, 2 contro 2 (ognuno con un compagno CPU) o cooperativa contro due CPU.
- **Allenamento**: tu contro la CPU, senza cronometro e senza limite di gol.

## Opzioni
- **Durata**: 2, 3 o 5 minuti, oppure senza limite. Pareggio a fine tempo: golden goal.
- **Gol per vincere**: libero, 3, 5, 7 o 10.
- **CPU**: facile, normale o difficile.
- **Visuale**: inclinata (3D) o dall'alto. In partita si cambia con V o con il tasto 3D sul telefono.

## Personalizza
Dal tasto **Personalizza** nel menu, con anteprima dal vivo:
- **Nametag**: il tuo nome (fino a 10 caratteri) e il colore dell'etichetta.
- **Texture della tua sfera**: classica, liscia, linee fitte, incrociate, spirale, pois, scacchi, zig-zag (sempre nel colore della tua squadra).
- **Pallone**: classico, a triadi in stile anni '70, cuoio retrò marrone, invernale arancione.
- **Taglio del prato**: strisce, orizzontali, scacchi, diagonali, rombi o cerchi.

Online l'avversario vede il tuo nome e la tua sfera; pallone e prato valgono solo sul tuo schermo.

## Stadio
L'erba c'è solo dentro le linee; attorno al campo ci sono una fascia grigia, i cartelloni, quattro torri faro e le tribune piene di tifosi a forma di sfera, che saltano quando la loro squadra segna.

## Comandi
| | Muovi | Tiro | Cross |
|---|---|---|---|
| Giocatore 1 (Rossi) | W A S D | Spazio | C (o Shift sinistro) |
| Giocatore 2 (Blu) | Frecce | Invio | Shift destro (o punto) |
| Touch (telefono in orizzontale) | joystick fisso in basso a sinistra (tocca e trascina ovunque nella metà sinistra) | tasto TIRA | tasto CROSS |

Online e in allenamento puoi usare sia WASD che le frecce. Esc o P: pausa (online il gioco non si ferma) · V: visuale · M: audio.

**Tiro e cross a carica.** Tieni premuto il tasto: la barra attorno alla tua sfera (e sul bordo del tasto, da telefono) si riempie in circa 0,8 secondi. Rilascia per calciare: più è piena, più il calcio è forte. Se la palla non è ancora vicina quando rilasci, il calcio parte appena la tocchi. Il tiro è rasoterra; il cross alza la palla, che passa sopra i giocatori e ricade dopo qualche rimbalzo. Una palla troppo alta sbatte sulla traversa e non è gol.

## Schermo intero su telefono
Su Android il gioco va a schermo intero quando inizi a giocare, e c'è un tasto apposito in alto a destra. Su iPhone Safari non permette lo schermo intero alle pagine web: usa Condividi → Aggiungi alla schermata Home e apri il gioco da lì.

## Tecnica
Un solo file HTML. Grafica con [Three.js](https://threejs.org/) r149, gioco online peer-to-peer con [PeerJS](https://peerjs.com/) 1.5.4 (WebRTC): il server pubblico gratuito di PeerJS serve solo a far trovare i due giocatori, poi i dati passano direttamente tra i due browser. Chi crea la stanza calcola la fisica, l'altro invia i comandi e riceve lo stato della partita. Per chi entra, la propria sfera si muove subito (predizione) e si riallinea dolcemente con lo stato dell'host, così non si sente il ritardo di rete. Nessun server proprio, nessuna build.
