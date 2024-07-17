Ciao ragazzi,
Esercizio di oggi: *Vue Slider*
nome repo: vue-slider

*Descrizione:*
Partendo dal markup della versione svolta in js plain, rifare lo slider ma questa volta usando Vue.

*Bonus:*
1- al click su una thumb, visualizzare in grande l'immagine corrispondente
2- applicare l'autoplay allo slider: ogni 3 secondi, cambia immagine automaticamente
3- quando il mouse va in hover sullo slider, bloccare l'autoplay e farlo riprendere quando esce

*Consigli del giorno:*
- regola d'oro: riciclare ovunque possibile! Questo significa che per la parte di markup possiamo recuperare html e css dell'esercizio svolto qualche giorno fa: è già tutto pronto!
- il riciclo spesso va a braccetto con le funzioni! Sapendole sfruttare bene, l'esercizio si riduce a poche righe ;)

Buon lavoro e buon divertimento!

<!-- SCOMPOSIZIONE PROBLEMA -->

1 - Rimuoviamo tutte le thumb presenti nell'HTML e ne lasciamo una sola che varrà per tutte grazie ad un v-for;
2 - Richiamiamo l'immagine di partenza tramite v-bind;
3 - Creiamo una variabile "activeImage" settata a 0;
4 - Ora diamo all'immagine di partenza :src="slides.image[activeImage]" Così che l'immagine grande corrisponda sempre a quella attiva;
5 - Creiamo due metodi per "prev" e "next";
6 - Il metodo next conterrà un IF per verificare se l'elemento attivo corrisponde all'ultimo elemento dell'array, in quel caso activeImage = 0;
6.1 : ALTRIMENTI activeImage++;
7 - Il metodo prev invece dovrà contenere un IF dove, nel caso in cui l'elemento attivo sia uguale a 0 allora activeImage = this.slides.length - 1;
7.1 ALTRIMENTI activeImage--;