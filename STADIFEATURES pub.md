Elenco funzioni di gioco RPG + mostri. Fatto da me e con commenti di Drk090 (iniziano con  --> )







- Avanti veloce
- Framerate smart che non fa scattare
-  Internazionalizza
-  associazione tasti personalizzati

* soldi
  * esistenza e comandi eventi per modificare (gamevar)
  * perdi se sconfitto (evento)
  * mamma tiene risparmi

- OVERWORLD
  - Camera centrata 
  - Pressione leggera del tasto direzionale cambia direzione senza movimento
  - Eventi (rpg maker)
  
    - Allenatori che ti notano
    - Due allenatori ti notano => battaglia in doppio
  - Tutte le possibilità di eventi di RPG maker (API per modificare il player e i suoi possedimenti (anche pk) dagli scrip)
  - Tutte le variabili e switch di rpg 
  - Metadati tiles
    - Collisioni/Passabilità 
      - Collisione fa suono di schianto
      - Collisione non impedisce al personaggio di muovere le gambe => rimosso, troppo lavoro per troppo poco guadagno. se viene naturalmente meglio
    - Livelli altezza
    - Bush flag (tileset di metadati per indicare le zone erba acqua grotta…)
    - Counter flag
    - altezza
  - mosse interagibili --> field moves
    - Taglio
    - Volo
    - Surf
    - Forza
    - Flash
    - Fossa
    - Teletrasporto
    - Covauova
    - Mulinello
    - Cascata
    - Spaccaroccia
    - Bottintesta
    - Profumino
    - Buon Latte
    - Sub
    - Forza Segreta
    - Scacciabruma
    - Scalaroccia
    - Schiamazzo (serve solo a registrare tracce audio)--> inutile?
  - Mezzi di movimento e luoghi dove sono consentiti
    - Corsa (e lock (auto press) introdotto in G4)
    - Bici normale (G1)
    -  Bici corsa (accelera, passa sabbia, decelera) (G3)
    -  Bici cross (impenna, saltella, salta dpad) (G3)
    -  Nave (signor marino)
  - Connessioni
  - Tile con comportamento
    - Ledge
    - Tiles animati
    - Tiles MN (cascata, mulinello)
    - Sub (interagisci)
    - Orme sulla sabbia (piedi e bici, astrarre-> orma veicolo, npc/sprite  sovrapposto?)
    - Acqua che riflette le persone e il cielo
    - Erba che si anima quando passi--> idem pozzanghere
    - mattonelle di ghiaccio della palestra
    - pietra friabile attraversabile con la bici
  - Spawn
    -  transizioni alla lotta
      -  fade
      -  quadratini
      -  spirale,
      -  ecc
    - erba acqua grotte
  - ​     Comparse massicce (G2)
    - ​     Molteplici nemici (G6?)
    - ​     https://wiki.pokemoncentral.it/Fenomeno
    - ​     mostri vaganti (G2) (eventi)
  - Giorno notte (G2) (dipende da RTC)
  - Meteo (G3)
  
    - pioggia
    - temporale (fulmini, effetto colori)
    - sabbia
  - Neve (grandine)
    PROPOSTE: 
    effetto climatico in base al luogo (clima) e stagione + effetto interni: quando piove e sei in casa senti il rumore della pioggia e se ci sono finestre i fulmini illuminano la stanza, mentre se sei in una grotta o in cantina non senti e non vedi nulla
  - Stagioni (G5) (dipende da RTC)
  - Abilità mostri fuori dalla lotta (G3)
  - Strumenti salvati (G1, migliorata sempre. G5: lista, e anche scene del menu). Strumenti base      (amo, ricerca strumenti) e strumenti normali (repellente. Richiesta di riuso G5)
    PROPOSTE: 
    funzione ordina e cerca (quando lo zaino è pieno di strumenti diventa difficile trovare quella determinata pozione!)
  - Mappe che appaiono sul navigatore in modo speciale (miraggio, suprema)
  - Eventi dipendenti che seguono il giocatore (G1)
  
  - primo mostro che segue il giocatore --> PROPOSTE: possibilità di attivare/disattivare feature e scegliere quale mostro ti segue e non per forza il primo in squadra, dare un senso a questa feature!! Come hanno fatto in let's go ad esempio.
    - allenatore che ti accompagna, lotta insieme a te e afine lotta cura la tua squadra
  - Aggiunta di strumenti alla musica di sfondo (G5) => sostituito da: comandi eventi musicali che permettono il fade e lo skip a un certo secondo della traccia 
  

 

- BATTAGLIA
  - vita, livello, stato, esperienza, sesso dei mostri in campo (HUD)--> status extra con modifica stat e roba simile, proprio come accade in showdown tanto per capirci
  - Menu
    - Mostri
      - info
      - scambia
    - Lotta (mostra mosse)
      - mostra PP rimanenti
      - mostra tipo mosse
      - efficacia mossa selez
      - Descrizione mossa
      - strumento tenuto(?)
    - Borsa
      - usa strumenti lotta e sfere
      - blocca il resto
    - fuga
      - calcolo
  - IA --> possibilità di scegliere il livello di difficoltà
  - Animazioni
    - Mosse 
    - Entrata
    - cambio forma
    - Idle
  - Tipi di oggetti di lotta
    - Mostri
    - Strumenti (usati e tenuti)       (G1, G2)
    - ​      Abilità (G3)
  - sistema battaglia
    - Battaglia scriptata (es rivale/lega messaggio, condizioni (per sconfitta , boss con caratteristiche speciali, ecc ), )  
    - si puo usare anche per IA?
    - Battaglia forzata/guidata ?
      - battaglia tutorial col professore con dialoghi o certe azioni bloccate
      
      - battaglia registrata, sui binari (lino, oldman) e con condizioni (es, non puo andare KO)
      
      - registratore lotte, replay (G4-5?)
      
    
    * Tipi di lotta (valutare se semplificabile con sistema eventi 
      * normale
        * allenatore
        * selvatico
      * Parco lotta
      * safari
  - ========== G1
    - eseguire mosse, danno
    
    - PP
      - mia versione: non è uno per ogni mossa ma uno per mostro, e mosse consumano più o meno (punti magia globali del mostro, come RPG normali)
      - scontro
      
    - Brutto colpo o altri modificatori danni. 
    
      versione mia: non è doppio, ma molto meno (es 1.2-1.3) ; non dipende dal caso ma da una statistica del mostro (designer stabilisca quale, se allenamento o una dedicata. e se esiste una corrispondente in difesa); oppure applicare un moltiplicatore che può variare in un range (es: 0.5-1.2) ad ogni attacco, a seconda della salute del mostro e altre condizioni
    
    - Efficacia tipo
    
    - Fuga
    
    - Cattura (mostriball ed effetti)
    
    - Velocità e ordine di azione
    
    - Verso (shifted per KO, involuto)
  - ========== G2
    
    - Nome allenatore (classe allenatore gen 1, sesso e immagine allenatore gen boh
    - meteo
  - ========== G3
    
    - Battaglia in doppio
  - ========== G4
    - Split fisico speciale
    - mosse con contatto
    - Capsule e bolli --> possibilità di cambiare tipo di ball una volta catturato il mostro
  - ========== G5
    - Battaglia in triplo e a rotazione--> lotta a round come nel dojo lotta (emerald), lotta automatica come nel palazzo lotta (sempre emerald) francamente odio questa modalità, ma potrebbe essere rivista per risolvere la lotta automaticamente qualore il giocatore non ne avesse voglia di lottare
    - Mostri non soprannominati       sono scritti in minuscolo con la prima lettera maiuscola
  - ========== G6
    - amicizia (!= da valore per ritorno e frustrazione?) --> meccanica come in 6 gen(?)
    

 



* vari contest come gara pigliamosche o gara di pesca (SMISTARE, forse overworld?)



- Menu
  - diario delle missioni
  - Mostri info
    - Max 6 (K)
    - Schermate diverse per aree diverse
    - possibilità di scambiare gli strumenti tenuti fra i diversi mostri in squadra
  - enciclopedia mostri
    --> funzione cerca, zone --> PROPOSTE: aggiunta learnset ed metodo di evoluzione
  - Navigatore/altro dispositivo
    - mappa
      - fiocchi
      - telefono
      - Radio --> il giocatore ha la possibilità di aggiungere le proprie tracce
      - feature extra di 4 gen (detector, controlla stato squadra, amicizia, stato uovo ecc.) --> HUD(?)
  - Giocatore
    - nome
    - immagine
    - Medaglie
    - Vedi e Personalizza aspetto
    - Tempo di gioco, data inizio gioco
    - firma
    - registra voce
    - altro
  - borsa
  - Opzioni
  - Salva
    - salva file
    - 1 salvataggio per profilo
    - profili multipli
  - Esci menu
  - esci gioco



*  filmato intro
  * coprights
  * animazione	
  * sostituito da: play video

 

* scena titolo
  * sfondo
  * premi start

* scena continua
  * nuovo gioco

  * opzioni

  * funzioni online

    * dono segreto e altre robe

  * continua
    * nome, location, completamento storia percentuale
    * faccine mostri posseduti
    
  * cambiare salvataggio: implementato con 1 solo salvataggio per personaggio, molteplici personaggi per utente del sistema operativo

    semplice opzione "scegli altri salvataggi" nel menu principale

    mia versione: scorrere a dx e sx sul bottone continua

  





* Minigiochi
  - Gare
  - Sotterranei
  - Basi segrete
  - Casinò
    - roulette
    - slot machine
    - "memory" col mostro a forma di palla o qualcosa del genere perchè vietato ai minori



 

 

 

- PC / centro mostri

  - Infermiera cura

    - cura
    - effetto sonoro
    - Ball nella macchina stesso colore ball usata
    - angolo dove cambiare nickname
    - angolo oppure campo di lotta sul retro dove si trovano move tutor e/o ricorda mosse

  - PC

    - deposita e ritira mostri

    - Sfondi box

    - Marchia mostri con simbolini

    - Seleziona più mostri insieme

    - Liberare

      - protezione softlock (see: pikasprey yellow)
    - disattivabile dopo molti avvisi
      
      

- RTC dependent (bacche, isole miraggio, ecc) (evento)

- Scambio

- Soft reset se tieni premuti tutti i tasti (qui magari fare un solo tasto dedicato)

 

- Utile creare una scena di selezione mostri generica, che puo essere configurata in base a cosa mostrare su ciascuno (capace (MT)/ abile, contest)
- sala d'onore
- avviso batteria sistema bassa
- avviso fare pausa ogni 45 min
- altri avvisi simpatici



- ATTENZIONE, ho confuso i dati di un mostro della ROM dai dati di un mostro catturato vivo e vegeto

  presente nella RAM / sav del giocatore e li ho messi nella stessa categoria. cercare di separare
- MOSTRI 
  - Personalità (ID)
  - soprannome
  - Allenatore originale
  - Evoluzione
  - livello, statistiche e mosse      (in lotta e in qualsiasi scena - > api msg globali)
    - Allenamento minigiochi
  - Squadra 6
  - Statistiche (EV IV, )
  - Tipo
  - Mosse 4
  - MT MN (G1), infinite (G5) (      Per evitare l'uso ripetuto di MT al fine di restaurare i PP, quando un      Pokémon dimentica una mossa in modo da impararne una da una MT o MN, la mossa imparata assume i PP della mossa sostituita. )
  - Condizione di stato 
    - più mia versione: i mostri hanno resistenze diverse a ciascuna condizione e al verificarsi del loro effetto. Invece che ad es. subire la % casuale della mossa, la % è nel mostro difensore e attaccante (es: un mostro di tipo erba sarà più bravo a applicare stati, e un mostro robusto a tollerarli)
    - Permanenti
      - Veleno
      - Paralisi
      - Sonno
      - Scottatura
      - Congelamento
    - volatili
    - Innamoramento
      - Confusione
  - Forme https://wiki.pokemoncentral.it/Differenze_di_forma (unown, spinda, rotom)
  - ======G2
  - Sesso, uova (differenze tra i sessi)
    - baby
    - cromatici
    - Affetto
    - Strumento tennuto
    - virus che migliora il guadagno di EV
  - ======G3

    - natura, abilità
    - Fiocchi e altri dati      personali memorizzati
  - ======G4
  - Doppia abilità tra cui scegliere




Aggiunte (no sapevo dove aggiungerle quindi le metto di seguito:
- virus aumenta guadagno evs--> possibili malattie con effetti negativi(?) gen 2
- Dono segreto gen 2
- Sistema per coltivare la bacche con fertilizaanti e simili gen 4
- Resume feature: come in3 gen
- Tasto aiuti/tutorials 3 gen
- Cercasfide 3 gen
- registra sfide ma non solo nel parco lotta, ma in tutte le lotte anche con i selvatici!
- GTS gen 4 
- foto commemorative gen 4 e 6 
- achievement system gen 5 
- cattura critica gen 5 

PROPOSTE:
- Quando lotti contro dei cattivi questi giocano sporco distraendo il tuo mostro (attacco fallisce), sparano al tuo mostro (lo danneggiano), il mostro del cattivo usa un colpo scorretto (aumento probabilità brutto colpo), ti impedisce di usare strumenti o di cambiare mostro ecc.

- Player home: una casa che man mano che effettui i vari upgrade ottieni l'orticello per le bacche, campo allenamento per ev training e move tutoring ecc.

- ne mancano altre, appena mi vengono in mente le scrivo ;)





 

