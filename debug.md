1° Bug
    • Il genere/Tags di ogni libro è "undefined"

2° Bug    
    • Manca l'immagine del 2° libro

3° Bug
    • Il tempo di lettura andrebbe arrotondato senza decimali
    • aggiunta l'unità di misura


4° Bug
    • Le icone degli ultimi 4 libri sono mancanti

5° Bug 
    • Nella maggior parrte dei libri mancano le stelle vuote


6° Bug
    • Le immagini escono fuori dai libri quando si rimpicciolisce la pagina    


7° Bug
    • è presente una costante che non viene mai utilizzata: genresLabels



Risoluzione:


1° Bug
    • Ci siamo accorti che il forEach ritorna sempre un "undefined" , per evitare questo problema abbiamo dichiarato la variabile fuori dal ciclo forEach per i generi, e abbiamo fatto sì che venisse modificata all'interno del forEach in modo che ad ogni iterazione venissero aggiunti i generi corrispondenti al libro attuale.

2° Bug 
    • Siamo andati ad aggiungere alla costante "chars" una proprietà aggiuntiva ovvero quella che rappresenta l'apostrofo assegnandole strigna vuota come valore. Questo ha fatto sì che il replace dei caratteri speciali per la traformazione del titolo nella corrispettiva immagine andasse a sostituire anche l'apostrofo nel titolo de "l'isola del tesoro".

3° Bug
    • Abbiamo aggiunto il metodo Math.round per arrotondare all'intero più vicino il numero di ore
    • Inoltre abbiamo aggiunto l'unità di misura (ore) al paragrafo che viene stampato in HTML


4° Bug    
    • Le icone mancavano poichè non tutti i generi avevano delle icone associate, per risolvere questo problema abbiamo fatto sì che in assenza di tale icona venga assegnata un'icona di default: 
    Abbiamo inizializzato una variabile assegnandogli la logica per la creazione dell'icona fuori dalla modifica dell'innerHTML dei libri, nel far questo abbiamo fatto in modo di sostituire gli spazi all'interno dei vari generi con un trattino basso, in modo che potessero esser scritti senza problemi all'interno degll'oggetto iconsByGenres. A questo punto abbiamo inserito una condizione per la quale, nel caso non sia definito il valore dell'icona da assegnare, venga assegnata l'icona del libro come default.


5° Abbiamo cambiato il numero di stelle vuote generate, facendo in modo che in base a se è presente o no la mezza stella, aggiunge un numero di stelle vuote per arrivare a 5 stelle totali.


6° Bug
    • Abbiamo aggiunto il rest per le immagini nel CSS
