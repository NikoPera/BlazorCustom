questa repo fa un fork di blazor js (v 8.0.2) e permette di richiamare Blazor.start() ogni volta che si vuole.

Se normalmente richiamare Blazor.start() è bloccato con errore "Blazor è gia stato avviato", in questo caso vado a pulire completamente:
- il circuito
- la connessione
- il dispatcher
- i componenti attuali e gli event handlers configurati (renderQueue -> renderer)
e permetto di ripartire..

Quindi (inevitabilmente) viene perso lo stato attuale, MA posso ricaricare Blazor senza effettuare un full-reload nei casi di circuito rotto.
