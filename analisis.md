## 4. Anàlisi de Dades
### Aplicacions de la IA
## **Introducció**
Google BigQuery amb AutoML permet analitzar grans volums de dades i construir models d'aprenentatge automàtic sense necessitat de programar en profunditat. Aquest manual et guiarà pas a pas per configurar i utilitzar aquesta eina.

#### Google BigQuery amb AutoML
- **Funcionalitat:** Permet analitzar dades massives i generar prediccions basades en IA.
- **Exemple pràctic:** Identificar patrons en el comportament dels usuaris per millorar les vendes.
- **Exemple de codi SQL:**
  ```sql
  SELECT * FROM predict_customer_behavior WHERE likelihood > 0.8;
## Impacte al Sector
- Millora la presa de decisions basada en dades.
- Redueix el temps i esforç necessari per a l'anàlisi de dades complexes.
- Proporciona eines accessibles per a usuaris no tècnics.

## Impacte Ambiental i Consells d'Eficiència
- **Consell 1:** Redueix la mida del dataset si no és necessari processar totes les dades.
- **Consell 2:** Entrena el model només quan sigui necessari (per exemple, un cop al mes).
- **Consell 3:** Configura l'ús d'infraestructura basada en energia renovable al Google Cloud Console.

## Propostes per Minimitzar l'Impacte
- Consolidar centres de dades per augmentar l'eficiència energètica.
- Reduir la freqüència d'entrenament de models si no és estrictament necessari.

# **Manual d’Ús de Google BigQuery amb AutoML per a l’Anàlisi de Dades**
---

## **Requisits Previs**
1. **Compte de Google Cloud:** Has de tenir un compte actiu.
2. **Projecte a Google Cloud:** Crea un projecte al [Google Cloud Console](https://console.cloud.google.com/).
3. **BigQuery activat:** Assegura't que BigQuery està habilitat al teu projecte.
4. **Dataset preparat:** Les teves dades han d'estar carregades a BigQuery.

---

## **Pas 1: Preparar el Dataset**
1. Accedeix al [Google BigQuery Console](https://console.cloud.google.com/bigquery).
2. Carrega les teves dades:
   - Clica a "Crea una taula".
   - Selecciona l’origen de les dades (arxiu CSV, JSON, etc.).
   - Defineix el nom del dataset i de la taula.
3. Assegura’t que les dades estiguin netes i estructurades (columnes amb noms clars i tipus de dades correctes).
<img src="https://miro.medium.com/v2/resize:fit:920/1*uoTzLiv72s6DqnlUge2qXQ.png" alt="Logo de BigQuery" width="800" height="400">
---

## **Pas 2: Crear un Model AutoML**
1. A la consola BigQuery, selecciona el teu dataset.
2. Fes clic a "Creació de model" (AutoML).
3. Configura els següents paràmetres:
   - **Taula d’entrenament:** Selecciona la taula que conté les teves dades.
   - **Variable objectiu:** Escull la columna que vols predir (per exemple, "probabilitat de compra").
   - **Tipus de model:** Classificació, regressió, o altres segons les teves necessitats.
4. Fes clic a "Entrenar model" i espera que el procés finalitzi.

---

## **Pas 3: Fer Prediccions**
1. Un cop creat el model, pots fer prediccions usant SQL.
2. Exemple de consulta SQL per predir resultats:
   ```sql
   SELECT customer_id, predicted_value
   FROM ML.PREDICT(MODEL `project_id.dataset_name.model_name`, 
                   TABLE `project_id.dataset_name.table_name`)
   WHERE predicted_value > 0.8;
Aquesta consulta retornarà només els clients amb una probabilitat superior al 80%.

## Pas 4: Optimització del Model
- **Anàlisi dels resultats:** Revisa les mètriques del model (precisió, sensibilitat, etc.).
- **Entrenament amb dades noves:** Actualitza el model amb dades més recents per millorar la seva precisió.


## Resolució de Problemes
- **Error en carregar dades:** Verifica que les columnes i tipus de dades siguin correctes.
- **Model no convergent:** Revisa que les dades estiguin ben balancejades (evita classes molt desproporcionades).
- **Costos elevats:** Configura límits de processament i revisions automàtiques per evitar càrrecs inesperats.

<img src="https://switchboard-software.com/wp-content/uploads/2023/06/Google-BigQuery.jpeg" alt="Logo de BigQuery" width="400" height="300">

## Conclusió
Google BigQuery amb AutoML és una eina versàtil que permet obtenir insights valuosos de les dades. Amb aquesta guia, podràs preparar les teves dades, entrenar models personalitzats i fer prediccions amb facilitat.
****
---
