---

copyright:
  years: 2016, 2017
lastupdated: "2017-05-23"

---


{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


#Servizi
{: #services}

I servizi disponibili sono elencati nel **Catalogo** sotto **Servizi** nella console {{site.data.keyword.Bluemix}}.
{:shortdesc}


I servizi predefiniti sono disponibili in {{site.data.keyword.Bluemix_notm}} per
le applicazioni mobili. {{site.data.keyword.Bluemix_notm}}
ti consente di implementare, ospitare o ingrandire facilmente questi servizi mobili per le tue applicazioni mobili. Potrai così concentrarti sulla logica e
sulla progettazione dell'applicazione.

{{site.data.keyword.Bluemix_notm}} ospita
e gestisce servizi middleware per le applicazioni Web. Gli sviluppatori
delle applicazioni possono specificare i servizi middleware di cui hanno bisogno. {{site.data.keyword.Bluemix_notm}} esegue quindi
automaticamente il provisioning di nuove istanze dei servizi middleware
specificati ed esegue il bind delle istanze del servizio all'applicazione.

{{site.data.keyword.Bluemix_notm}} visualizza i servizi in due modi: per categoria del servizio e per tipo di supporto del servizio.



<dl>
<dt><strong>Categoria</strong></dt>
<dd>I servizi {{site.data.keyword.Bluemix_notm}}
sono organizzati in diverse categorie. In ciascuna categoria del servizio,
i servizi creati da IBM vengono elencati per primi, seguiti dai servizi di terze parti e, infine,
dai servizi della community.</dd>
<dt><strong>Supporto</strong></dt>
<dd>Per i servizi {{site.data.keyword.Bluemix_notm}} vengono forniti più livelli di supporto. La seguente tabella descrive le informazioni di supporto generali per i servizi {{site.data.keyword.Bluemix_notm}}:

</dd>
</dl>



|Tipo	|Descrizione	|Dettagli sul supporto|
|:------|:--------------|:--------------|
|IBM	|Un servizio fornito da IBM e che è generalmente disponibile.	|Viene fornito supporto per i problemi considerati come un difetto
in un servizio fornito da IBM generalmente disponibile. Il supporto viene fornito in base alla severità da te impostata. Per ulteriori informazioni sulla severità dei ticket, vedi [Come contattare il supporto](/docs/support/index.html#contacting-bluemix-support).|
|Terze parti	|Un servizio fornito da un'azienda diversa da IBM.	|Il supporto per i servizi di terze parti è fornito dal
fornitore del servizio. Se un problema viene analizzato da IBM e tale problema viene considerato come un difetto in un servizio di terze parti, IBM non è tenuto a fornire una correzione. IBM condividerà l'analisi con il fornitore del servizio di terze parti laddove necessario.|
|Community	|Un servizio fornito da una community
open source.	|Il supporto per i servizi di community viene fornito dalla Community di sviluppatori {{site.data.keyword.Bluemix_notm}}. Se un problema viene analizzato da IBM e tale problema viene considerato come un difetto in un servizio di community, IBM non è tenuto a fornire una correzione.|
|Beta	|Un servizio che non è pronto per la produzione ed è a una
fase di sviluppo di prova. Un servizio beta può aiutare i team di sviluppo
e di marketing a valutare la qualità dei servizi prima di
renderli generalmente disponibili.	|Viene fornito supporto per i problemi considerati come un difetto in un servizio beta fornito da IBM, tuttavia  IBM non è tenuto a fornire una correzione. Inoltre,
laddove applicabile, al ticket del problema verrà assegnata una severità 3 o 4. Per informazioni sulla severità dei ticket, vedi [Come contattare il supporto](/docs/support/index.html#contacting-bluemix-support).|
{: caption="Tabella 1. Informazioni sul supporto dei servizi {{site.data.keyword.Bluemix_notm}}" caption-side="top"}




{{site.data.keyword.Bluemix_notm}} offre anche dei servizi sperimentali che puoi provare. Per visualizzare tutti i servizi sperimentali, i contenitori tipo e i runtime disponibili, accedi a {{site.data.keyword.Bluemix_notm}}, scorri fino alla fine del Catalogo e fai clic su **Catalogo Lab {{site.data.keyword.Bluemix_notm}}**.

I servizi sperimentali potrebbero non essere stabili e possono cambiare secondo modalità non compatibili con le versioni precedenti. L'uso di questi servizi negli ambienti di produzione è sconsigliato. Il supporto per i servizi sperimentali viene fornito tramite la Community di sviluppatori {{site.data.keyword.Bluemix_notm}}. Se un problema viene analizzato da IBM
e tale problema viene considerato come un difetto in un servizio sperimentale,
IBM non è tenuto a fornire una correzione.

Per utilizzare un servizio nella console {{site.data.keyword.Bluemix_notm}}, nell'interfaccia riga di comando cf, in IBM {{site.data.keyword.Bluemix_notm}} DevOps Services o in qualsiasi strumento supportato, attieniti alla seguente procedura:

1. Crea un'istanza del servizio. Nella maggior parte dei casi,
l'istanza del servizio può essere creata quando crei l'applicazione.

2. Identifica l'applicazione che utilizza la nuova istanza del servizio. Per le applicazioni Web, puoi specificare più di un'applicazione per
utilizzare la stessa istanza del servizio, in genere per la condivisione dei dati.

3. Scrivi il codice nella tua applicazione per consentire l'integrazione con il
servizio.

# Aggiunta di un servizio alla tua applicazione
{: #add_service}


{{site.data.keyword.Bluemix}} ha un elenco di servizi e
li gestisce per conto degli sviluppatori. Per aggiungere un servizio a
un'applicazione da utilizzare, devi richiedere un'istanza di tale servizio e configurare l'applicazione in modo
che interagisca con il servizio.

Puoi visualizzare tutti i servizi disponibili in {{site.data.keyword.Bluemix_notm}}
nei seguenti modi:

* Dall'interfaccia utente {{site.data.keyword.Bluemix_notm}}. Visualizza il catalogo {{site.data.keyword.Bluemix_notm}}.
* Dall'interfaccia riga di comando cf. Utilizza il comando **cf marketplace**.
* Dalla tua applicazione. Utilizza la [API di servizi GET /v2/services ![Icona link esterno](../icons/launch-glyph.svg)](http://apidocs.cloudfoundry.org/197/services/list_all_services.html){: new_window}.

Puoi selezionare il servizio di cui hai bisogno quando sviluppi le applicazioni. Dopo la tua selezione, {{site.data.keyword.Bluemix_notm}} interagisce con il servizio ed
effettua le operazioni necessarie per eseguire il provisioning delle risorse del servizio. Il processo di provisioning può essere
differente per i diversi tipi di servizi. Ad esempio, un servizio database crea un database e un
servizio di notifiche di push per le applicazioni mobili genera le informazioni di configurazione.

{{site.data.keyword.Bluemix_notm}} fornisce le risorse di un servizio alla tua applicazione utilizzando un'istanza del servizio. Un'istanza del servizio può essere condivisa tra le
applicazioni Web.

Se vi sono dei servizi disponibili in altre regioni, potrai utilizzare anche tali
servizi. Questi servizi devono essere accessibili da Internet e avere degli endpoint API. Per utilizzare
questi servizi, devi codificare manualmente l'applicazione nello stesso modo in cui codifichi le applicazioni
esterne o gli strumenti di terze parti per utilizzare i servizi {{site.data.keyword.Bluemix_notm}}. Per ulteriori informazioni, vedi [Abilitazione di applicazioni esterne e strumenti di terze parti all'utilizzo di servizi {{site.data.keyword.Bluemix_notm}}](#accser_external).



## Richiesta di una nuova istanza del servizio
{: #req_instance}

Per richiedere una nuova istanza del servizio, devi utilizzare la console {{site.data.keyword.Bluemix_notm}} o l'interfaccia riga di comando cf.

**Nota:** quando specifichi il nome servizio, evita di utilizzare caratteri che non siano alfabetici o numerici; in caso contrario, i risultati potrebbero essere imprevedibili.

Se utilizzi la console {{site.data.keyword.Bluemix_notm}} per richiedere un'istanza del servizio, completa la seguente procedura:

1. Nel {{site.data.keyword.Bluemix_notm}} **Catalogo**, fai clic sul tile per il servizio che vuoi aggiungere. Viene visualizzata la pagina dei dettagli.

2. Nel riquadro Aggiungi servizio, seleziona un'applicazione di cui desideri eseguire il bind a questa istanza del servizio dall'elenco **Applicazione**.

3. Immetti un nome nel campo **Nome servizio**. Viene fornito un nome servizio predefinito. Puoi modificare il nome nel campo o lasciarlo invariato.

4. Completa le selezioni o i campi aggiuntivi e fai quindi clic su **CREA**.

Se utilizzi l'interfaccia riga di comando cf per richiedere un'istanza del servizio, completa la seguente procedura:

1. Utilizza il comando **cf marketplace** per trovare il nome e il piano del servizio di cui hai bisogno.

2. Utilizza il seguente comando per creare un'istanza del servizio, dove nome_servizio è il nome del servizio, piano_servizio è il piano del servizio e istanza_servizio è il nome da utilizzare per questa istanza del servizio.

    ```
    cf create-service nome_servizio piano_servizio istanza_servizio
    ```

3. Utilizza il seguente comando per eseguire il bind dell'istanza del servizio a un'applicazione, dove nome_applicazione è il nome dell'applicazione e istanza_servizio è il nome dell'istanza del servizio.

    ```
    cf bind-service nome_applicazione istanza_servizio
    ```

Puoi eseguire il bind a un'istanza del servizio per le sole istanze dell'applicazione che si trovano nello stesso spazio od organizzazione. Tuttavia, puoi utilizzare istanze di servizio provenienti da altri spazi od organizzazioni seguendo le modalità adottate dalle applicazioni esterne. Invece di creare un bind, utilizza le credenziali per configurare direttamente l'istanza della tua applicazione. Per ulteriori informazioni sull'uso dei servizi {{site.data.keyword.Bluemix_notm}} da parte delle applicazioni esterne, vedi [Abilitazione di applicazioni esterne all'utilizzo dei servizi {{site.data.keyword.Bluemix_notm}} ](#accser_external).


## Configurazione della tua applicazione per l'interazione con un servizio
{: #config}

Dopo aver eseguito il bind di un'istanza del servizio all'applicazione, devi configurare
l'applicazione in modo da interagire con il servizio.

Ciascun servizio potrebbe richiedere un meccanismo differente per comunicare con le applicazioni. Questi
meccanismi sono documentati come parte della definizione del servizio a scopo informativo quando sviluppi le
applicazioni. Per congruenza, i meccanismi sono richiesti perché la tua applicazione interagisca con il
servizio.

* Per interagire con i servizi del database, utilizza le informazioni fornite da {{site.data.keyword.Bluemix_notm}}, quali ID utente, password
e l'URI di accesso per l'applicazione.
* Per interagire con i servizi di back-end mobili, utilizza le informazioni fornite da {{site.data.keyword.Bluemix_notm}}, quali l'identità dell'applicazione
(ID applicazione), le informazioni di sicurezza specifiche per il client e l'URI di accesso per
l'applicazione. I servizi mobili di norma operano in contesto reciproco e, pertanto, le informazioni
di contesto, come il nome dello sviluppatore dell'applicazione e l'utente che utilizza l'applicazione,
possono essere condivise tra la serie di servizi.
* Per interagire con le applicazioni Web o il codice cloud lato server per le applicazioni mobili, utilizza le
informazioni fornite da {{site.data.keyword.Bluemix_notm}}, quali le
credenziali di runtime nella variabile di ambiente *VCAP_SERVICES*
dell'applicazione. Il valore della variabile di ambiente *VCAP_SERVICES* è la
serializzazione di un oggetto JSON. La variabile contiene i dati di runtime richiesti per interagire con i servizi
a cui è associata l'applicazione. Il formato dei dati è differente per i
diversi servizi. Potresti dover leggere la documentazione del servizio in merito a cosa aspettarsi
e come interpretare ogni elemento di informazione.

Se si verifica un arresto anomalo di un servizio di cui esegui il bind a un'applicazione,
l'esecuzione dell'applicazione potrebbe essere arrestata oppure potrebbero verificarsi per essa delle condizioni di errore. {{site.data.keyword.Bluemix_notm}} non riavvia automaticamente l'applicazione per eseguire un ripristino da tali problemi. Valuta una codifica della tua applicazione per identificare interruzioni, eccezioni ed errori di connessione e per eseguire il ripristino da tali condizioni. Per ulteriori informazioni, vedi l'argomento di risoluzione dei problemi relativo al fatto che [le applicazioni non verranno riavviate automaticamente](/docs/troubleshoot/index.html#ts_topmenubar).

## Abilitazione di applicazioni esterne all'utilizzo dei servizi {{site.data.keyword.Bluemix_notm}}
{: #accser_external}

Potresti disporre di applicazioni create ed eseguite
all'esterno di {{site.data.keyword.Bluemix_notm}},
o utilizzare strumenti di terze parti. Se i servizi {{site.data.keyword.Bluemix_notm}} forniscono chiavi del servizio accessibili da Internet, puoi utilizzare questi servizi con le tue applicazioni locali e con gli strumenti di terze parti.

I seguenti servizi forniscono le chiavi del servizio per l'utilizzo esterno:

* {{site.data.keyword.amashort_old}} <!--Advanced Mobile Access-->
* {{site.data.keyword.alchemyapishort}} <!--AlchemyAPI-->
* {{site.data.keyword.alertnotificationshort}} <!--Alert Notification-->
* {{site.data.keyword.sparks}} <!--Analytics for Apache Spark-->
* {{site.data.keyword.appseccloudshort}} <!--Application Security on Cloud-->
* {{site.data.keyword.blockchain}} <!--Blockchain-->
* {{site.data.keyword.cloudant}} <!--Cloudant&reg; NoSQL DB-->
* {{site.data.keyword.iotmapinsights_short}} <!--Context Mapping-->
* {{site.data.keyword.conversationshort}} <!--Conversation-->
* {{site.data.keyword.dashdbshort}} <!--dashDB-->
* {{site.data.keyword.discoveryshort}} <!--Discovery-->
* {{site.data.keyword.documentconversionshort}} <!--Document Conversion-->
* {{site.data.keyword.iotdriverinsights_short}} <!--Driver Behavior-->
* {{site.data.keyword.geospatialshort_Geospatial}} <!--Geospatial Analytics-->
* {{site.data.keyword.GlobalizationPipeline_short}} <!--Globalization Pipeline-->
* {{site.data.keyword.appconserviceshort}} <!--IBM&reg; App Connect-->
* {{site.data.keyword.dataworks_short}} <!--IBM&reg; Data Connect-->
* {{site.data.keyword.graphshort}} <!--IBM&reg; Graph-->
* {{site.data.keyword.iotelectronics_full}} <!--IBM&reg; IoT for Electronics-->
* {{site.data.keyword.twittershort}} <!--Insights for Twitter-->
* {{site.data.keyword.iot4auto_short}} <!--IoT for Automotive-->
* {{site.data.keyword.iotinsurance_short}} <!--IoT for Insurance-->
* {{site.data.keyword.languagetranslatorshort}} <!--Language Translator-->
* {{site.data.keyword.dwl_short}} <!--Lift-->
* {{site.data.keyword.messagehub}} <!--Message Hub-->
* {{site.data.keyword.mobileanalytics_short}} <!--Mobile Analytics-->
* {{site.data.keyword.nlclassifiershort}} <!--Natural Language Classifier-->
* {{site.data.keyword.objectstorageshort}} <!--Object Storage-->
* {{site.data.keyword.personalityinsightsshort}} <!--Personality Insights-->
* {{site.data.keyword.HybridConnect_short}} <!--Product Insights-->
* {{site.data.keyword.mobilepush}} <!--Push-->
* {{site.data.keyword.retrieveandrankshort}} <!--Retrieve and Rank-->
* {{site.data.keyword.speechtotextshort}} <!-- Speech to Text-->
* {{site.data.keyword.streaminganalyticsshort}} <!--Streaming Analytics-->
* {{site.data.keyword.texttospeechshort}} <!--Text to Speech-->
* {{site.data.keyword.toneanalyzershort}} <!--Tone Analyzer-->
* {{site.data.keyword.tradeoffanalyticsshort}} <!--Tradeoff Analytics-->
* {{site.data.keyword.weather_short}} <!--Weather Company Data-->
* {{site.data.keyword.workloadscheduler}} <!--Workload Scheduler-->

Per abilitare un'applicazione esterna o uno strumento di terze parti
a utilizzare un servizio {{site.data.keyword.Bluemix_notm}},
completa la seguente procedura:

1. Richiedi un'istanza del servizio.
    1. Nel Dashboard nell'interfaccia utente {{site.data.keyword.Bluemix_notm}}, fai clic su **Utilizza servizi o API**. Viene visualizzato il Catalogo.
    2. Dal Catalogo, seleziona il servizio che vuoi facendo clic sul relativo tile. Viene visualizzata la pagina dei dettagli.
    3. Nella finestra Aggiungi servizio, mantieni la selezione dell'elenco **Applicazione**: come **Lascia senza binding**. Questa selezione significa che
il servizio non sarà connesso a un'applicazione {{site.data.keyword.Bluemix_notm}}.
    4. Opera le altre selezioni come necessario. Fai quindi clic su **CREA**. Viene creata un'istanza del servizio e viene visualizzato il dashboard del servizio.
2. Nel riquadro di navigazione del dashboard del servizio, puoi selezionare **Credenziali del servizio** per visualizzare o aggiungere credenziali in formato JSON. Utilizza la chiave API visualizzata come credenziali per stabilire una
connessione all'istanza del servizio.

La tua applicazione che viene eseguita esternamente a {{site.data.keyword.Bluemix_notm}} può
ora accedere al servizio {{site.data.keyword.Bluemix_notm}}.

**Nota:** se vuoi eliminare delle istanze del servizio oppure controllare le informazioni di fatturazione, devi tornare indietro al Dashboard nell'interfaccia utente per gestire le istanze del servizio.

## Creazione di un'istanza del servizio fornito dall'utente
{: #user_provide_services}

Puoi avere delle risorse che sono gestite esternamente a {{site.data.keyword.Bluemix_notm}}. Se hai delle credenziali per accedere a queste risorse esterne da Internet, puoi creare delle istanze del servizio fornito dall'utente {{site.data.keyword.Bluemix_notm}} per rappresentare le risorse esterne e comunicare con esse.

Per creare un'istanza del servizio fornito dall'utente ed eseguirne il bind a un'applicazione, completa la seguente procedura:

1. Crea un'istanza del servizio fornito dall'utente utilizzando il comando **cf create-user-provided-service** oppure il comando **cf cups**:
    * Per creare un'istanza del servizio fornito dall'utente generale, utilizza l'opzione **-p** e
separa i nomi parametro con delle virgole. L'interfaccia riga di comando cf ti chiede quindi ciascun
parametro, uno alla volta. Ad
esempio:
        ```
        cf cups testups1 -p "host, port, dbname, username, password"
        host> pubsub01.example.com
        port> 1234
        dbname> sampledb01
        username> pubsubuser
        password> p@$$w0rd
        Creating user provided service testups1 in org my-org / space dev as user@sample.com...
        OK
        ```

    * Per creare un'istanza del servizio che scarica informazioni in un software di gestione di log di terze parti,
utilizza l'opzione **-l** e specifica la destinazione fornita dal software di gestione di log di terze parti. Ad
esempio:

        ```
        cf cups testups2 -l syslog://example.com
        Creating user provided service testups2 in org my-org / space dev as user@sample.com...
        OK
        ```

    Se vuoi aggiornare uno o più parametri dell'istanza del servizio fornito dall'utente, utilizza il comando **cf update-user-provided-service** oppure
il comando **cf uups**.

    * Per aggiornare un'istanza del servizio fornito dall'utente, utilizza l'opzione **-p**
e specifica le chiavi e i valori di parametro in un oggetto json. Ad
esempio:

        ```
        cf uups testups1 -p "{\"username\":\"pubsubuser2\",\"password\":\"p@$$w0rd2\"}"
        Updating user provided service testups1 in org my-org / space dev as user@sample.com...
        OK
        ```

    * Per creare un'istanza del servizio che scarica informazioni in un software di gestione di log di terze parti, utilizza l'opzione -l. Ad
esempio:

        ```
        cf uups testups2 -l syslog://example2.com
        Updating user provided service testups2 in org my-org / space dev as user@sample.com...
        OK
        ```

2. Esegui il bind dell'istanza del servizio alla tua applicazione utilizzando il comando cf bind-service. Ad
esempio:

	```
	cf bind-service myapp testups1
	Binding service testups1 to app myapp in org my-org / space dev as user@sample.com...
	OK
	```

Ora puoi configurare la tua applicazione per utilizzare le risorse esterne. Per informazioni su come configurare la tua applicazione per interagire con un servizio, vedi [Configurazione della tua applicazione per l'interazione con un servizio](#config){: new_window}.

## Utilizzo dei servizi in un'altra regione
{: #cross_region_service}

Se disponi di un'istanza di servizio creata e associata mediante bind ad applicazioni in un'unica regione, puoi utilizzare questa istanza in un'altra regione utilizzando uno dei seguenti metodi:

  * Utilizza le credenziali del servizio per configurare direttamente l'istanza della tua applicazione. Per i dettagli, vedi [Abilitazione di applicazioni esterne all'utilizzo dei servizi {{site.data.keyword.Bluemix_notm}}](#accser_external).
  * Crea come ponte un servizio fornito dall'utente.

	Supponiamo di iniziare nella regione in cui
desideri utilizzare l'istanza del servizio. Per utilizzare un'istanza del servizio che si trova
in un'altra regione, completa la seguente procedura:

      1. Passa alla regione in cui si trova l'istanza del servizio. Nella barra dei menu di {{site.data.keyword.Bluemix_notm}}, espandi il menu **Regione** e quindi seleziona la regione in cui si trova l'istanza del servizio.

      2. Recupera le credenziali e i parametri di connessione dalla variabile di ambiente VCAP_SERVICES dell'istanza del servizio nella regione in cui si trova il servizio. Completa la seguente
procedura:

	       1. Nel Dashboard {{site.data.keyword.Bluemix_notm}}, fai clic sul tile dell'applicazione. Viene visualizzata la pagina Panoramica.
	       2. Nel riquadro di navigazione, fai clic su **Variabili di ambiente**. Vengono visualizzati i dettagli della variabile di ambiente *VCAP_SERVICES*. Registra il contenuto JSON per l'istanza
del servizio.

      3. Passa alla regione in cui desideri utilizzare l'istanza del
servizio. Nella barra dei menu di {{site.data.keyword.Bluemix_notm}}, espandi il menu **Regione** e quindi seleziona la regione in cui vuoi utilizzare l'istanza del servizio.

      4. Crea un'istanza del servizio fornito dall'utente utilizzando le credenziali
e i parametri di connessione che hai registrato dalla variabile di ambiente
*VCAP_SERVICES*. Per informazioni su come creare un'istanza
del servizio fornito dall'utente, vedi [Creazione di un'istanza
del servizio fornito dall'utente](#user_provide_services).

      5. Esegui il bind dell'istanza del servizio fornito dall'utente alla tua applicazione
utilizzando il seguente comando:

	     ```
	     cf bind-service myapp user-provided_service_instance
	     ```






## Utilizzo di servizi in un altro servizio
{: #s2s_binding}

Autorizzazione accesso al servizio consente a un servizio di accedere a un altro servizio direttamente. Puoi autorizzare e configurare l'accesso di un'istanza del servizio ad altre istanze del servizio sul Dashboard {{site.data.keyword.Bluemix_notm}}.

Per utilizzare un'istanza del servizio da un altro servizio, completa la seguente procedura:

1. Nel Dashboard {{site.data.keyword.Bluemix_notm}}, fai clic sul tile per il servizio a
cui vuoi accedere. Viene visualizzato il dashboard per il servizio.
2. Nel riquadro di navigazione, fai clic su **Gestisci** per autorizzare il bind da altre istanze del servizio utilizzando la console dell'istanza del servizio.
3. Se vuoi negare ad altri servizi l'accesso all'istanza, fai clic su **Autorizzazione accesso al servizio** nel riquadro di navigazione e utilizza quindi **Revoca** per rimuovere il bind del servizio.
