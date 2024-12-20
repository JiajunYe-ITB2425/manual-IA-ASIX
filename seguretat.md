## 2. Aplicacions de la IA a la informàtica

La Intel·ligència Artificial (IA) ha transformat de manera radical el camp de la informàtica, oferint solucions que van des de l'automatització de tasques repetitives fins a la millora de la seguretat en entorns complexos. A continuació, s'exploren les aplicacions generals i específiques de la IA, amb exemples pràctics i implicacions tècniques.

### 2.1 Ús general en la informàtica

#### **Automatització de processos**
- **Objectiu:** Reduir la intervenció humana en tasques repetitives i susceptibles a errors, com la gestió de registres, actualitzacions de sistemes o configuracions periòdiques.
- **Exemple pràctic:** Sistemes d’automatització com **Ansible** i **Puppet**, que incorporen IA per detectar configuracions òptimes i aplicar canvis de manera autònoma.
- **Impacte:** Augmenta la velocitat i precisió dels processos, permetent als professionals centrar-se en tasques més crítiques.

#### **Seguretat cibernètica**
- **Funcions principals:**
  - Identificar patrons d'atac mitjançant l'anàlisi d'anomalies en temps real.
  - Automatitzar la resposta a incidents, com bloquejar un atac de phishing o aïllar una màquina compromesa.
- **Tecnologies destacades:**
  - **SIEM amb IA (com Splunk o QRadar):** Agreguen i analitzen dades de seguretat a gran escala per detectar comportaments anòmals.
  - **SOAR:** Plataformes que automatitzen la resposta a incidents amb l’ajuda d’algorismes d'IA.
- **Benefici clau:** Reducció del temps de resposta davant amenaces, minimitzant l'impacte de les vulnerabilitats.

#### **Monitorització de rendiment**
- **Finalitat:** Garantir l'eficiència dels sistemes identificant problemes abans que afectin el servei.
- **Aplicacions:**
  - Anàlisi predictiva per identificar saturacions en servidors o xarxes.
  - Ajustament automàtic de paràmetres com la càrrega del CPU o l'assignació de memòria.
- **Cas real:** **Dynatrace**, una plataforma que utilitza IA per monitoritzar aplicacions en temps real, anticipant possibles problemes de rendiment.

---

### 2.2 Aplicació específica en l'Administració de Sistemes Informàtics en Xarxa

En l'àmbit d'ASIX, la IA es converteix en una eina essencial per optimitzar la gestió de sistemes i xarxes, donant suport als administradors en entorns cada vegada més complexos i interconnectats.

#### **Detecció d'amenaces**
- **Com funciona:**
  - Algorismes d’aprenentatge automàtic entrenats amb milions de mostres de dades per identificar activitats malicioses en el trànsit de xarxa.
  - Exemples d’aplicacions:
    - Reconèixer patrons d'atacs DDoS.
    - Identificar intents de connexió no autoritzats.
- **Exemple destacat:** **Darktrace**, que actua com un “sistema immunitari digital” detectant i responent a anomalies en temps real.

#### **Gestió proactiva**
- **Objectiu:** Anticipar-se a fallades i minimitzar el temps d'inactivitat.
- **Metodologia:**
  - Algorismes predictius que analitzen logs de sistemes per anticipar avaries en maquinari.
  - Predicció del consum de recursos futurs basant-se en dades històriques.
- **Exemple real:** **AWS CloudWatch** utilitza IA per predir problemes d'escalabilitat en entorns d'infraestructura com a servei (IaaS).

#### **Optimització del rendiment**
- **Funció principal:** Configuració automàtica de paràmetres crítics com:
  - L’equilibri de càrrega en entorns virtualitzats.
  - L'ajustament de la qualitat del servei (QoS) en xarxes congestionades.
- **Benefici clau:** Garantir un ús eficient dels recursos, reduint costos i millorant la qualitat del servei.

#### **Suport a la virtualització**
- **Impacte:** La IA millora la distribució i gestió de recursos en plataformes de virtualització com **VMware**, **Hyper-V** o **Proxmox**.
- **Casos d'ús:**
  - Redistribuir màquines virtuals en temps real segons la càrrega.
  - Identificar màquines virtuals inactives per optimitzar l'ús d'energia.

---

### 2.3 Altres aplicacions generals

- **Automatització d'auditories de seguretat:**
  - La IA pot analitzar configuracions i polítiques de seguretat per detectar desviacions o incompliments normatius.
- **Intel·ligència predictiva en tallafocs:**
  - Implementació d’algorismes que ajusten les regles automàticament per respondre a patrons d'atac emergents.
- **Monitorització de xarxes amb IA adaptativa:**
  - Sistemes que ajusten les seves estratègies de supervisió segons el comportament de la xarxa.

---

### 2.4 Exemples destacats

- **Darktrace:** Utilitza IA per analitzar trànsit en xarxes i respondre a amenaces en temps real.
- **Splunk:** Analitza grans quantitats de dades per oferir informació accionable sobre rendiment i seguretat.
- **Elasticsearch:** Plataforma per monitoritzar i analitzar dades de logs, ideal per entorns ASIX. Tot i que no és exclusivament una eina de seguretat, Elasticsearch s'utilitza sovint en la seguretat per indexar i cercar logs de sistemes, ajudant a detectar activitats sospitoses mitjançant l'anàlisi de dades en temps real.

---

### 2.5 Guia per a la utilització i configuració de cada una d'aquestes IAs: explicació detallada de les eines

## Darktrace

## Objectiu del Cas Pràctic

El propòsit d’aquesta guia és mostrar com utilitzar Darktrace per identificar i respondre a una amenaça de seguretat dins d'una xarxa empresarial. En aquest cas pràctic, detectarem un intent d'intrusió d'un dispositiu extern que vol accedir a un servidor intern i aplicarem mesures per protegir la infraestructura.

---

## Pas 1: Instal·lació i Configuració Inicial de Darktrace

### 1. **Obtenció de Darktrace**
   - **Passos per obtenir Darktrace:**
     - Accedeix al lloc web oficial de [Darktrace](https://www.darktrace.com) i crea un compte. Si ets una empresa, podràs sol·licitar una demostració personalitzada.
     - Un cop obtinguis la llicència o la versió de prova, descarrega l’arxiu d’instal·lació que correspon a la teva infraestructura (Linux o Windows).
   
   - **Instal·lació del software:**
     - Executa l'instal·lador i segueix les instruccions per completar la instal·lació a un servidor centralitzat o a la màquina des d'on controlaràs la seguretat de la xarxa.

### 2. **Integració amb la Xarxa**
   - **Connexió a la Xarxa:**
     - Darktrace necessita ser connectat als dispositius clau de la teva infraestructura, com switches i routers, per poder analitzar el trànsit de dades en temps real.
     - La plataforma utilitza sensors que es col·loquen al punt d'entrada de la xarxa o a les capes més profundes de la infraestructura per capturar informació sobre les comunicacions entre dispositius.
   
   - **Visibilitat completa:**
     - Un cop instal·lat i configurat, Darktrace podrà visualitzar tot el trànsit de la xarxa, incloent comunicacions internes i externes.


### 3. **Configurar les Polítiques de Seguretat**
   - **Definir el que és normal:**
     - Darktrace necessita entendre què és "normal" dins de la teva xarxa. Això inclou configurar qui pot accedir a què (per exemple, quins dispositius poden comunicar-se amb quins servidors), quins protocols són segurs i quines aplicacions són autoritzades.
     - Utilitzant aquesta informació, Darktrace pot identificar comportaments anòmals basant-se en una comparativa de les activitats actuals amb les "normes" establertes.

---

## Pas 2: Monitorització en Temps Real

### 1. **Accedir a la Consola de Darktrace**
   - **Inici de sessió i visibilitat general:**
     - Accedeix a la consola web de Darktrace mitjançant el navegador. La interfície gràfica és intuïtiva, amb un tauler centralitzat que mostra l'estat de la xarxa i alertes en temps real.
     - Visualitza l’estat de la teva xarxa: dispositius connectats, trànsit de dades, i alertes de seguretat.

       [![Captura-de-pantalla-de-2024-12-13-12-15-18.png](https://i.postimg.cc/2yzG3sQJ/Captura-de-pantalla-de-2024-12-13-12-15-18.png)](https://postimg.cc/JD2Z2ddc)
       _Figura 1: Interfaz web de Darktrace mostrando análisis de patrones de vida y alertas de anomalías._

### 2. **Revisió de la Visibilitat en Temps Real**
   - **Panell de control:**
     - El panell de Darktrace et permet veure tot el trànsit de dades que circula per la xarxa, així com identificar els dispositius connectats. Els dispositius són representats per icones amb codis de colors:
       - **Verde:** El dispositiu està actiu i comportant-se de manera normal.
       - **Taronja/Vermell:** S'ha detectat un comportament sospitós que pot indicar una amenaça.

      ![image](https://github.com/user-attachments/assets/e3bda879-b358-4534-ba0e-6ab7e924cace)

       _Figura 2: En la Sección inferior de Darktrace cada alerta indica un comportamiento o evento inusual en la red que podría ser una amenaza potencial._
         
   - **Explorar dispositius:**
     - Clicant sobre qualsevol dispositiu, pots veure detalladament el seu trànsit de dades, les connexions establertes, i l'analítica de comportament de la IA de Darktrace.

       ![image](https://github.com/user-attachments/assets/8192ac69-2099-4472-9855-0b31918ae888)
       _Figura 3: Podemos ver la sección de Device Admin en la cual encontramos para la monitorización, gestión y clasificación de dispositivos._


---

## Pas 3: Identificació d'una Amenaça en Xarxa

### 1. **Detectar Comportaments Anòmals**
   - **Exemple pràctic:**
     - Imagina que un portàtil s'ha connectat a la xarxa de l'empresa i està intentant accedir a un servidor que normalment no té accés.
     - Darktrace analitza el trànsit d'aquest dispositiu i detecta que el comportament és anòmal perquè no coincideix amb els patrons previs de connexió.
   
   - **Alertes i anàlisi:**
     - Quan Darktrace detecta una amenaça, emet una alerta. A la consola, es mostrarà un banner de notificació vermell que indica que s'ha detectat una activitat sospitosa.
     - Les alertes inclouen informació detallada sobre:
       - **Dispositiu sospitós**: Qui està causant la inquietud (per exemple, un portàtil o un dispositiu mòbil).
       - **Adreces IP implicades**: Les adreces IP de les parts involucrades en la connexió.
       - **Anàlisi del comportament**: Una descripció de l'activitat que es considera anòmala, com intentant accedir a serveis no autoritzats o enviant una quantitat anormal de dades.

### 2. **Revisar l’Alerta de Seguretat**
   - Fes clic sobre l'alerta per veure els detalls de la possible amenaça. A la pàgina d'anàlisi, es mostraran:
     - Les adreces IP implicades en l'incident.
     - Els dispositius de la xarxa que poden estar involucrats.
     - L'historial de les connexions i els moments exactes de la detecció.

---

## Pas 4: Resposta a l'Amenaça

### 1. **Aïllar el Dispositiu Sospitós**
   - **Resposta autònoma:**
     - Si tens habilitada la funció de resposta autònoma, Darktrace aïllarà automàticament el dispositiu compromès de la xarxa, tallant així qualsevol connexió malintencionada que pugui estar intentant establir.
   - **Resposta manual:**
     - Si prefereixes controlar-ho manualment, pots seleccionar el dispositiu sospitós i activar l'opció d'aïllar el dispositiu de la xarxa per evitar que segueixi causant danys.

### 2. **Anàlisi de la Xarxa per Amenaces Addicionals**
   - Un cop el dispositiu sospitós ha estat aïllat, és fonamental realitzar una revisió profunda de la resta de la xarxa per identificar altres possibles vulnerabilitats.
   - Darktrace generarà un informe amb la informació necessària per ajudar-te a identificar altres dispositius que poden estar compromesos.

---

## Pas 5: Generar Informes i Millorar la Seguretat

### 1. **Generació d'Informes**
   - **Detalls de l'incident:**
     - Un cop resolt l'incident, Darktrace generarà un informe complet que inclou:
       - El dispositiu compromès.
       - L’activitat sospitosa detectada.
       - Les accions que es van prendre per mitigar la amenaça.
     - Aquest informe és útil per a auditories i per ajustar les polítiques de seguretat a futur.

### 2. **Ajustar Polítiques de Seguretat**
   - **Revisió i millora de les polítiques:**
     - Un cop analitzat l’incident, revisa les teves polítiques de seguretat. Si detectes que una vulnerabilitat va permetre l’incident, ajusta les regles per evitar que es repeteixi.
     - Darktrace permet establir regles més estrictes per als dispositius, com per exemple limitar l'accés a recursos interns o aplicar controls més estrictes sobre els ports i protocols autoritzats.

---

## Pas 6: Monitorització Continuada

### 1. **Monitorització Post-Incident**
   - **Seguiment continu:**
     - És important seguir monitoritzant la xarxa després d’un incident per identificar qualsevol possible nova amenaça. Darktrace et permet continuar amb la supervisió i detectar comportaments inusuals que podrien indicar nous intents d'intrusió.

### 2. **Alertes en Temps Real**
   - **Reviseu alertes:**
     - La teva tasca com a responsable de la seguretat de la xarxa és revisar regularment les alertes de seguretat. Darktrace et mantindrà informat de qualsevol activitat sospitosa que es produeixi en temps real.

---

## Conclusió

Aquesta guia t'ha proporcionat una explicació detallada de com utilitzar Darktrace per detectar, respondre i mitigar amenaces a la teva xarxa. Amb una combinació de seguretat automatitzada i anàlisi intel·ligent, Darktrace et permet protegir la teva infraestructura davant de possibles intrusions de manera eficaç. Tant si tens experiència en seguretat com si ets un usuari novell, Darktrace és una eina que facilita la protecció de la teva xarxa de manera intuitiva i potent.

---
## 3. Impacte al sector

La IA en el sector de la informàtica, i en particular en ASIX, està transformant la forma en què es gestionen i supervisen els sistemes. Tot i els nombrosos avantatges, també presenta alguns reptes.

### 3.1 Avantatges
- **Eficiència millorada:** Processos automatitzats i supervisió constant redueixen els temps de resposta davant problemes.
- **Decisions més precises:** Els models d'aprenentatge automàtic proporcionen prediccions fiables per a la presa de decisions basada en dades.
- **Innovació contínua:** L'adaptació automàtica a nous patrons d'atac permet mantenir la seguretat en evolució constant.

### 3.2 Inconvenients
- **Dependència tecnològica:** Hi ha el risc de confiar massa en solucions automàtiques, la qual cosa pot reduir les habilitats humanes en entorns crítics.
- **Costos elevats:** Les solucions avançades basades en IA sovint requereixen inversions significatives en maquinari, llicències i formació.
- **Riscos de biaix en IA:** Algorismes mal entrenats poden prendre decisions errònies, la qual cosa pot tenir conseqüències greus en matèria de seguretat.

---

## 4. Impacte ambiental

### 4.1 Consum energètic
Els models d'Intel·ligència Artificial (IA) requereixen una gran quantitat de recursos computacionals per ser entrenats i operatius, fet que genera un impacte ambiental significatiu:

- **Entrenament de models:** Les xarxes neuronals, especialment les grans (com GPT o BERT), necessiten milions de processaments per ajustar els seus paràmetres. Això comporta un consum elèctric elevat. 
  - *Exemple:* Entrenar un únic model de IA pot generar emissions de CO₂ equivalents a les produïdes per diversos vols transatlàntics. Això es deu a l’ús intensiu de processadors com GPUs (unitats de processament gràfic) o TPUs (unitats de processament tensorial) en centres de dades.
- **Centres de dades:** Aquests espais alberguen milers de servidors, que han de funcionar constantment, generant calor i requerint sistemes de refrigeració avançats. Es calcula que els centres de dades consumeixen aproximadament un 1% de tota l’energia global.
  - *Dades preocupants:* Es preveu que el consum elèctric dels centres de dades s’incrementi exponencialment amb el creixement de la IA i altres tecnologies relacionades.

### 4.2 Residus electrònics
L'impacte de la IA no es limita al consum energètic; també contribueix significativament a la generació de residus electrònics:
- **Renovació constant de maquinari:** Per suportar la creixent complexitat dels algoritmes, les empreses necessiten actualitzar constantment el maquinari, la qual cosa produeix equips obsolets a gran escala.
- **Dificultat en el reciclatge:** Els components avançats dels servidors, com plaques base o xips especialitzats, sovint són difícils de reciclar i acaben en abocadors, contaminant el medi ambient amb metalls pesants i materials tòxics.
  - *Exemple:* Es calcula que només un 20% dels residus electrònics a nivell mundial es reciclen adequadament.

---

## 5. Propostes per minimitzar els impactes ambientals

### 5.1 Eficiència energètica
Optimitzar l'ús de l'energia en la implementació i entrenament de models d'IA pot reduir significativament l'impacte ambiental. Algunes accions clau són:

- **Optimització dels algorismes:** Crear models més petits i eficients que puguin oferir resultats similars als dels models grans però amb un menor consum d’energia. Exemples d'això inclouen:
  - *Pruned models*: Reducció de parts no necessàries d'un model sense comprometre la precisió.
  - *Quantized models*: Representació més simple de paràmetres per reduir càlculs.
- **Centres de dades verds:** Prioritzar l'ús d'energia renovable en els centres de dades. Per exemple:
  - **Google** opera centres de dades alimentats amb energia 100% renovable.
  - **Microsoft** busca ser *carbon-negative* abans del 2030.
- **Ubicació estratègica:** Construcció de centres de dades en llocs amb climes freds per reduir la necessitat de refrigeració.

### 5.2 Reutilització i reciclatge
És fonamental establir pràctiques per gestionar adequadament els residus electrònics generats per la IA:
- **Programes de reciclatge corporatius:** Empreses tecnològiques poden implementar plans per desmantellar i reutilitzar components de maquinari en lloc de simplement descartar-los. 
  - *Exemple:* HP i Dell tenen programes dedicats al reciclatge de maquinari.
- **Donacions:** Els equips que encara són funcionals poden ser reutilitzats per escoles, ONG o comunitats amb recursos limitats, evitant així que es converteixin en residus.
- **Materials reciclables:** Invertir en la fabricació de components amb materials més sostenibles i fàcils de reciclar, com plàstics biodegradables i metalls reutilitzables.

### 5.3 Desenvolupament sostenible
El compromís amb la sostenibilitat és essencial per reduir l'impacte ambiental de la IA a llarg termini:
- **Recerca i desenvolupament en eficiència:** Invertir en la creació de tecnologies d'IA que consumeixin menys energia sense comprometre el rendiment. Això inclou nous tipus de processadors més eficients i sistemes d’entrenament distribuït.
- **Polítiques corporatives sostenibles:** Les empreses han de:
  - Comprometre’s amb objectius de neutralitat de carboni.
  - Participar en programes globals com el **Climate Neutral Data Centre Pact**, que promou centres de dades sostenibles a Europa.
- **Promoció de la computació federada:** Reduir la centralització de dades distribuint les operacions de càlcul entre dispositius finals. Això disminueix la necessitat de grans centres de dades per a certes tasques d'IA.

---
## Conclusió 

La Intel·ligència Artificial ha demostrat ser una eina poderosa en l'administració de sistemes informàtics en xarxa. La seva capacitat per automatitzar processos, millorar la seguretat i augmentar l'eficiència operativa ofereix grans avantatges, especialment en tasques repetitives i en la detecció de ciberamenaces. Gràcies a la IA, els administradors de xarxa poden centrar-se en qüestions més estratègiques i complexes, optimitzant recursos i temps.

Tanmateix, també presenta una sèrie de reptes i inconvenients. La dependència tecnològica pot reduir la capacitat dels professionals per intervenir manualment en situacions d'emergència, la qual cosa podria posar en perill la seguretat dels sistemes. A més, els costos elevats associats a la implementació de la IA i el seu impacte ambiental, degut al consum energètic i la generació de residus electrònics, són aspectes que cal abordar.

Per garantir que la IA es converteixi en una força positiva per a la societat, és fonamental adoptar mesures responsables, com la creació de models més eficients energèticament i l'ús de fonts d'energia renovables en els centres de dades. Només així podrem assegurar-nos que la IA no només millora les nostres xarxes i sistemes, sinó que també contribueix a un futur més sostenible i equitatiu.



