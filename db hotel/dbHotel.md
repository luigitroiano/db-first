# database name : Hotel
# nome tabella : 
<!-- TABELLA clienti -->
- id int mediumint PRIMARY KEY NOT NULL  AUTO_INCREMENT 
- nome string VARCHAR(20) NOT NULL
- cognome string VARCHAR(20) NOT NULL
- indirizzo string VARCHAR(200) NOT NULL
- telefono int VARCHAR(15) NOT NULL 

<!-- TABELLA camere -->
- numero_camera int PRIMARY KEY SMALLINT NOT NULL
- piano int TINYINT NOT NULL
 - tipo string VARCHAR(20) NOT NULL <!--'singola','doppia','matrimoniale','tripla' -->
 - letti_aggiunti int TINYINT NOT NULL 
 - optionals string VARCHAR(20) NOT NULL<!--'fumatori','ariaCondizionata','vistaMare','tv' -->

<!-- TABELLA prezzi -->
- checkin date DATE NOT NULL
- checkout date DATE NOT NULL
- tipo_camera string VARCHAR(20) NOT NULL <!--'singola','doppia','matrimoniale','tripla' -->
- prezzo int DOUBLE(6,2) NOT NULL  

<!-- TABELLA supplementi -->
- codice int PRIMARY KEY TINYINT NOT NULL AUTO_INCREMENT
- voce VARCHAR(20) NOT NULL
- prezzo int DOUBLE(5,2) NOT NULL

<!-- TABELLA prenotazioni -->
- id int PRIMARY KEY MEDIUMINT NOT NULL AUTO_INCREMENT
- id_cliente int FK MEDIUMINT NOT NULL
- checkin date DATE NOT NULL
- checkout date DATE NOT NULL 
- camera int FK SMALLINT NOT NULL
- prezzoTotale int DOUBLE(7,2) NOT NULL

<!-- TABELLA  supplementi_prenotati-->
- id_prenotazione int FK MEDIUMINT NOT NULL
- codice_supplemento int FK TINYINT NOT NULL 

