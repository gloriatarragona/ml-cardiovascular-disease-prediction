# Predicció de Malalties Cardiovasculars amb Aprenentatge Automàtic

Aquest repositori conté un projecte d’aprenentatge automàtic enfocat a la **predicció i prevenció de malalties cardiovasculars** utilitzant dades clíniques. El projecte s’ha desenvolupat com a part d’una assignatura universitària d’*Investigació Operativa* i explora diverses tècniques d’aprenentatge supervisat.

## Visió General del Projecte

Les malalties cardiovasculars són una de les principals causes de mort a nivell mundial. L’objectiu d’aquest projecte és desenvolupar models que ajudin a la detecció precoç i estratificació de risc d’aquestes malalties mitjançant mètodes d’aprenentatge automàtic.

Apliquem i comparem tres algorismes d’aprenentatge supervisat:

- Regressió Logística  
- Gradient Boosting Trees  
- Random Forest

El focus està posat a maximitzar la **recall**, per tal de reduir el nombre de falsos negatius — identificant tants pacients en risc com sigui possible.

## Conjunt de Dades

- **Font:** [Kaggle - Cardiovascular Disease Dataset](https://www.kaggle.com/datasets/colewelkins/cardiovascular-disease/data)  
- **Font Original:** [UCI Machine Learning Repository - Heart Disease](https://archive.ics.uci.edu/dataset/45/heart+disease)  
- **Mida:** ~70.000 registres  
- **Llicència:** Open Data Commons  
- **Variables:** Edat, sexe, colesterol, glucosa, IMC, pressió arterial, factors d’estil de vida, etc.  
- **Variable objectiu:** Presència (`1`) o absència (`0`) de malaltia cardiovascular.

##  Anàlisi Exploratori de Dades

- Detecció i filtratge d’outliers (eliminació d'observacions amb valors irrealistes)  
- Eliminació de variables multicolineals (per exemple, alçada i pes en favor de l’IMC)  
- Estadístiques descriptives i gràfics de distribució  
- Anàlisi de correlació

## 🤖 Models i Mètodes

### Regressió Logística
- Simple i interpretable  
- Regularitzada amb Ridge (`C=1`)  
- Umbral optimitzat per prioritzar la sensibilitat

### Gradient Boosting Trees
- Captura relacions no lineals complexes  
- S’ha ajustat amb grid search en `n_estimators` i `max_depth`  
- Anàlisi de la importància de variables via impuritat Gini i valors SHAP

### Random Forest
- Robusta davant soroll i sobreajustament  
- Estratègia d’ajust similar a GBT  
- Inclou també visualització de la importància de variables

##  Mètriques d’Avaluació

Tots els models es van avaluar utilitzant:

- **Accuracy**  
- **Precision**  
- **Recall** 
- **F1-Score**

| Model               | Accuracy | Recall   |
|---------------------|----------|----------|
| Regressió Logística | 0.73     | 0.73     |
| Gradient Boosting   | 0.74     | 0.69     |
| Random Forest       | 0.73     | 0.68     |

##  Conclusions 

- **Variables més rellevants:**  
  - Pressió arterial sistòlica alta  
  - Edat  
  - IMC (Índex de Massa Corporal)  
  - Colesterol alt

- La **Regressió Logística** va oferir els resultats més equilibrats i interpretables.

##  Treball Futur

- Explorar més models (p. ex., xarxes neuronals o SVM)  
- Incloure conjunts de dades externs amb perfils de risc més diversos  
- Col·laborar amb professionals de la salut per a validació clínica  
- Considerar el desplegament d’una eina web senzilla per a la predicció de risc

##  Tecnologia Utilitzada

- Python 3  
- scikit-learn  
- pandas, NumPy, matplotlib, seaborn  
- SHAP (per explicabilitat)  
- Jupyter Notebook

##  Autors

- Toni Esteve Gené  
- Gloria Tarragona Ruiz  
- Ainhoa Trillo Rodríguez
  
 Gener 2025 — Universitat Autònoma de Barcelona
