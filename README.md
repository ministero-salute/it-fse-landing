# Landing page del progetto

## Repository
### Gateway
1. [it-fse-gtw-config](https://github.com/ministero-salute/it-fse-gtw-config)

Il microservizio in oggetto ha la responsabilità di gestire e persistere le configurazioni del Gateway condivise tra tutti i microservizi.

2. [it-fse-gtw-dispatcher](https://github.com/ministero-salute/it-fse-gtw-dispatcher)  

Il microservizio in oggetto ha la responsabilità di esporre al Consumer le API Rest per l'invio, la cancellazione, la sostituzione e l'aggiornamento metadati di un documento clinico.

3. [it-fse-gtw-eds-client](https://github.com/ministero-salute/it-fse-gtw-eds-client)

Il microservizio in oggetto ha la responsabilità di gestire la comunicazione verso l'EDS.

4. [it-fse-gtw-fhir-mapping-engine](https://github.com/ministero-salute/it-fse-gtw-fhir-mapping-engine)

Il microservizio in oggetto ha la responsabilità di effettuare la trasformata di un CDA in un bundle FHIR tramite FHIR Mapping Language.

5. [it-fse-gtw-garbage](https://github.com/ministero-salute/it-fse-gtw-garbage)

Il microservizio in oggetto ha la responsabilità di gestire la Data Retention su MongoDB, effettuando la pulizia dei record correttamente inviati o obsoleti.

6. [it-fse-gtw-indexer](https://github.com/ministero-salute/it-fse-gtw-indexer)

Il microservizio in oggetto ha la responsabilità di richiamare il microservizio it-fse-gtw-ini-client per l'indicizzazione dei documenti su INI e, in caso di successo, richiamare il microservizio it-fse-gtw-publisher.

7. [it-fse-gtw-ini-client](https://github.com/ministero-salute/it-fse-gtw-ini-client)

Il microservizio in oggetto ha la responsabilità di gestire la comunicazione con INI.

8.  [it-fse-gtw-publisher](https://github.com/ministero-salute/it-fse-gtw-publisher)

Il microservizio in oggetto ha la responsabilità di richiamare il microservizio it-fse-gtw-eds-client per eseguire la pubblicazione su EDS.

9.   [it-fse-gtw-rules-manager](https://github.com/ministero-salute/it-fse-gtw-rules-manager)

Il microservizio in oggetto ha la responsabilità di recuperare dall'EDS le regole sintattiche, semantiche, terminologiche e di mapping.

10.  [it-fse-gtw-status-check](https://github.com/ministero-salute/it-fse-gtw-status-check)

Il microservizio in oggetto ha la responsabilità di esporre al Consumer le API per verificare lo stato delle validazioni e pubblicazioni effettuate su FSE2.0.

11. [it-fse-gtw-status-manager](https://github.com/ministero-salute/it-fse-gtw-status-manager)

Il microservizio in oggetto ha la responsabilità di accogliere e salvare i log di stato provenienti dai microservizi del Gateway al fine di permettere ad it-fse-gtw-status-check l'esposizione verso il Consumer.

12.  [it-fse-gtw-validator](https://github.com/ministero-salute/it-fse-gtw-validator) 

Il microservizio in oggetto ha la responsabilità di effettuare la validazione sintattica, semantica e terminologica del documento fornito in input.

### Monitoring
1. [it-fse-monit-be-external-info-writer](https://github.com/ministero-salute/it-fse-monit-be-external-info-writer)

Il microservizio espone un'API REST pubblica e consente la fornitura dei dati circa le indicizzazioni e le prestazioni relative alle strutture sanitarie.

2. [it-fse-monit-be-kpi-reader](https://github.com/ministero-salute/it-fse-monit-be-kpi-reader)

Il microservizio espone una REST API che consente di interrogare i KPI generati.

3. [it-fse-monit-be-kpi-writer](https://github.com/ministero-salute/it-fse-monit-be-kpi-writer)

Il microservizio genera gli indicatori di performance a partire dai dati forniti sulle prestazioni e sulle indicizzazioni e nel rispetto delle regole di calcolo definite dal decreto riparto.

4. [it-fse-monit-be-report-reader](https://github.com/ministero-salute/it-fse-monit-be-report-reader)

Il microservizio espone una REST API che consente di generare file di reportistica per rendicontazione sui KPI in formato `PDF` e `CSV`.

5. [it-fse-monit-fe-react](https://github.com/ministero-salute/it-fse-monit-fe-react)

Single Page Application che rappresenta il front-end del sistema di monitoraggio.

### EDS 
1. [it-fse-datarepo-data-quality](https://github.com/ministero-salute/it-fse-datarepo-data-quality)

Il microservizio in oggetto ha la responsabilità di verificare la qualità del Bundle FHIR proveniente dal Gateway e verificare l'aderenza alla FHIR Normative R4.

2. [it-fse-datarepo-fhir-server](https://github.com/ministero-salute/it-fse-datarepo-fhir-server)

Il microservizio in oggetto ospita il Server FHIR.

3. [it-fse-datarepo-processor](https://github.com/ministero-salute/it-fse-datarepo-processor)

Il microservizio in oggetto ha la responsabilità di finalizzare la pubblicazione su EDS: recupera il Bundle FHIR, effettua la deduplicazione, richiama it-fse-datarepo-data-quality per procedere con la validazione e finalizza l'operazione sul Server FHIR.

4. [it-fse-srv-dictionary](https://github.com/ministero-salute/it-fse-srv-dictionary)

Il microservizio in oggetto espone API che consentono la creazione, lettura, aggiornamento ed eliminazione di dizionari e codifiche terminologiche. Il microservizio, inoltre, espone API necessarie al Gateway per effettuare l'allineamento dei nuovi dizionari.

5. [it-fse-srv-fhir](https://github.com/ministero-salute/it-fse-srv-fhir)

Il microservizio in oggetto espone API che consentono la creazione, lettura, aggiornamento ed eliminazione delle regole di mapping utilizzati dal Gateway in fase di pubblicazione. Il microservizio, inoltre, espone API necessarie al Gateway per effettuare l'allineamento delle nuove regole.

6. [it-fse-srv-ingestion](https://github.com/ministero-salute/it-fse-srv-ingestion)

Il microservizio in oggetto ha la responsabilità di accogliere le operazioni di pubblicazione provenienti dal Gateway.

7. [it-fse-srv-log-ingestion](https://github.com/ministero-salute/it-fse-srv-log-ingestion)

Il microservizio in oggetto ha la responsabilità di accogliere i log strutturati provenienti dal Gateway.

8. [it-fse-srv-query](https://github.com/ministero-salute/it-fse-srv-query)

Il microservizio in oggetto ha la responsabilità di comunicare con il Server FHIR ed esporre interfacce REST verso gli altri microservizi.

9. [it-fse-srv-semantic-rules-manager](https://github.com/ministero-salute/it-fse-srv-semantic-rules-manager)

Il microservizio in oggetto espone API che consentono la creazione, lettura, aggiornamento ed eliminazione degli artefatti per i controlli semantici utilizzati dal Gateway in fase di validazione. Il microservizio, inoltre, espone API necessarie al Gateway per effettuare l'allineamento dei nuovi artefatti.

10.  [it-fse-srv-syntax-rules-manager](https://github.com/ministero-salute/it-fse-srv-syntax-rules-manager)

Il microservizio in oggetto espone API che consentono la creazione, lettura, aggiornamento ed eliminazione degli artefatti per i controlli sintattici utilizzati dal Gateway in fase di validazione. Il microservizio, inoltre, espone API necessarie al Gateway per effettuare l'allineamento dei nuovi artefatti.

### Provisioning
1. [it-fse-prov-be-antivirus-client](https://github.com/ministero-salute/it-fse-prov-be-antivirus-client)

Il microservizio in oggetto ha la responsabilità di invocare il servizio per la scansione degli artefatti utilizzati per generare nuovi certificati.

2. [it-fse-prov-be-ca-client](https://github.com/ministero-salute/it-fse-prov-be-ca-client)

Il microservizio in oggetto ha la responsabilità di invocare il servizio per la generazione/revoca/rinnovo dei certificati necessari all'utilizzo dei servizi esposti dal Gateway.

3. [it-fse-prov-be-notifier](https://github.com/ministero-salute/it-fse-prov-be-notifier)

Il microservizio in oggetto ha la responsabilità di notificare per email all'Attore di interesse il verificarsi di un evento.

4. [it-fse-prov-be-orchestrator](https://github.com/ministero-salute/it-fse-prov-be-orchestrator)

Il microservizio in oggetto ha la responsabilità di orchestrare le richieste emesse dall'Utente verso gli opportuni microservizi in grado di soddisfarle.

5. [it-fse-prov-be-requests](https://github.com/ministero-salute/it-fse-prov-be-requests)

Il microservizio in oggetto ha la responsabilità di gestire le richieste di generazione/revoca/rinnovo di certificati.

6. [it-fse-prov-be-users](https://github.com/ministero-salute/it-fse-prov-be-users)

Il microservizio in oggetto ha la responsabilità di gestire l'organigramma con cui si definiscono i ruoli degli utenti registrati nell'applicativo.

7. [it-fse-prov-fe-react](https://github.com/ministero-salute/it-fse-prov-fe-react)

Single Page Application che rappresenta il front-end del sistema di provisioning.

### FTS - Terminology System
1. [it-fse-gtw-exporter](https://github.com/ministero-salute/it-fse-gtw-exporter)

Il microservizio in oggetto ha la responsabilità di esportare sul repository https://github.com/ministero-salute/it-fse-catalogs gli artefatti sintattici, semantici e terminologici usati dal Gateway.

2. [it-fse-srv-converter](https://github.com/ministero-salute/it-fse-srv-converter)

Il microservizio in oggetto ha la responsabilità di convertire una terminologia nei formati CUSTOM_CSV, CUSTOM_JSON, FHIR_R4_JSON e FHIR_R4_XML.

3. [it-fse-srv-dictionary](https://github.com/ministero-salute/it-fse-srv-dictionary)

Il microservizio in oggetto ha la responsabilità di esporre le api di authoring per l'inserimento di terminologie sul Terminology Server.

4. [it-fse-srv-policy-manager](https://github.com/ministero-salute/it-fse-srv-policy-manager)

Il microservizio in oggetto ha la responsabilità di censire gli utenti del terminology server e di notificarli quando avviene un cambiamento sui terminology artifact.

5. [it-fse-srv-predictive-maintainer](https://github.com/ministero-salute/it-fse-srv-predictive-maintainer)

Il microservizio in oggetto ha la responsabilità di creare un Codesystem in stato draft sul Terminology Server a partire dalle loggate strutturate emesse dal Gateway.

6. [it-fse-srv-query](https://github.com/ministero-salute/it-fse-srv-query)

Il microservizio in oggetto ha la responsabilità di interfacciarsi con il Terminology Server in FHIR.

7. [it-fse-srv-terminology-server](https://github.com/ministero-salute/it-fse-srv-terminology-server)

Il microservizio in oggetto ospita il Terminology Server FHIR.

8. [it-fse-prov-be-notifier](https://github.com/ministero-salute/it-fse-prov-be-notifier)

Il microservizio in oggetto ha la responsabilità di notificare per email all'Attore di interesse il verificarsi di un evento.

### Supporto

1. [it-fse-gtw-tools](https://github.com/ministero-salute/it-fse-gtw-tools)

Il repository in oggetto contiene i tools di supporto al corretto utilizzo del FSE2.0.

2. [it-fse-gtw-test-container](https://github.com/ministero-salute/it-fse-gtw-test-container)

Il repository in oggetto contiene containers che consentono di avviare istanze locali delle entità presenti sul Fascicolo Sanitario Elettronico 2.0.
