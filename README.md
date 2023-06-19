# Array img Carousel

- creo l'array di immagini
- prendo un elemento dal DOM dove inserirò le immagini
    - **FINO A CHE** ho immagini nell'array:
        - Iserisco un immagine dell'array nel DOM
    - L'immagine attiva avrà una classe che gli permetterà di mostrarsi (active) tutte le altre saranno nascote
- prendo due elementi dal DOM che funzioneranno da bottoni in ascolto di click (bottone avanti e bottone indietro)

    - Al click sul bottone avanti:
        - **SE** l'indice di posizione(\*) va sopra la lunghezza massima(**):
            - Lo metto al valore di partenza
        - Prendo tutte le immagini del carousel del DOM
        - Seleziono da quello che preso un immagine (che sarà al momento attiva):
            - per selezionarla uso l'indice di posizione(\*) della lista in cui si trova
        - Rimuovo la classe active all'immagine che al momento è attiva
        - Incremento di uno l'indice della mia selezione della lista, cosi seleziono l'immagine successiva
        - Aggiungo la classe active all'immagine successiva selezionata
    - Al click sul bottone indietro:
        - Stesse azioni del bottone avanti ma cambia:
            - il **SE**, che diventa: l'indice di posizione(\*) va sotto zero:
                - Lo metto al valore massimo, (**)il valore massimo lo stabilisco grazie alla lunghezza dell'array di immagini
            - l' incremento dell'indice di posizione della lista diventa un decremento, cosi da selezionare l'immagine precedente

