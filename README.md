# hello-world-web-maven

Lo scopo  di questo progetto e' soltanto di far vedere un esempio di progetto maven.
Una volta creato il progetto maven ( si puo' fare sia dalla linea di comando che da un IDE ) questi sono i passaggi da seguire:
- Apro il prompt dei comandi dentro il percorso della cartella del progetto.
- Lancio il comando `mvn clean install`, il quale mi crea il file war del progetto dentro la cartella `target`.
- Creo una cartella `dist` in cui andro' a mettere tutti gli eseguibili e metto li' dentro il file war creato.
Adesso inizia la fase di deployment:
- Copio questo file dentro la cartella `webapps` di Tomcat.
- Avvio Tomcat il quale si crea una copia del progetto al suo interno.
- Apro il browser e digitando `http://localhost:8080/nome_progetto/` si aprira' il progetto sul web.  

# See
* Per vedere lo stesso progetto senza utilizzare maven [Clicca qui](https://github.com/sandrus88/hello-world-web).



