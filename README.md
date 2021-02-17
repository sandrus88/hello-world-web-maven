# hello-world-web-maven

Lo scopo di questo progetto e' di creare un progetto web maven.

Il codice sorgente e' lo stesso usato nei esempi jsp/servlet dentro il progetto [hello-world-web](https://github.com/sandrus88/hello-world-web).<br/>
Mentre per vedere una descrizione completa di un progetto Maven puoi vedere [project_mvn](https://github.com/sandrus88/project_mvn)

### Download and Build the project
Puoi scaricare il file di distribuzione `.war` presente nel percorso `./dist/hello-world-web-maven.war` oppure compilare e fare build usando Maven.

```
git clone https://github.com/sandrus88/hello-world-web-maven.git
cd hello-world-web-maven
mvn clean install
```

Fai deploy del file `.war` presente ora nella cartella `target` nel tuo `application server`.


### Deploy in Tomcat

Copia il file `.war` nella cartella `%CATALINA_HOME%\webapps`. 

Se i parametri sono impostate corretamente, `unpackWARs="true"` e `autoDeploy="true"`, nel file di configurazione `%CATALINA_HOME%\conf\server.xml` 
l'`application server` esplodera' il file war in una cartella con lo stesso nome e fara' il deploy dell'applicazione.

```
<Server ...>
    <Service name="Catalina">
        <Connector port="8080" protocol="HTTP/1.1" connectionTimeout="20000" redirectPort="8443" />
        <Engine name="Catalina" defaultHost="localhost">
            <Host name="localhost"  appBase="webapps"
                  unpackWARs="true" autoDeploy="true">
                ...    
            </Host>
        </Engine>
    </Service>
</Server>
```

Se non is desidera attivare l'`unpackWAR` si pu' usare il `manager` di Tomcat per effettuare l'installazione dell'applicazione.

### Test the App

`http://localhost:8080/hello-world-web-maven/`

# See

* [project_mvn](https://github.com/sandrus88/project_mvn) - Progetto Semplice Maven
* [hello-world-web](https://github.com/sandrus88/hello-world-web) - Progetto originale Web con i jsp/servlet



