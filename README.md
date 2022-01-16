# Pràctica Kaggle APC UAB 2021-22
### Nom: Emil Carvajal Viteri
### DATASET: URL Classification
### URL: [https://www.kaggle.com/shawon10/url-classification-by-naive-bayes/data](http://....)
## Resum
El dataset utilitza dades de URL's.
Tenim 1562978 dades amb 2 atributs. Un atribut representa la URL i l'altre la categoria al cual pertany. En total hi han 15 categories.
### Objectius del dataset
Com el dataset només té URL's i la seva classificació, volem aprender a classificar les URL amb alguna tècnica d'aprenentatge computacional.
## Experiments
Durant aquesta pràctica hem realitzat diferents experiments:
* Variant el tamany del dataset manualment
* Utilitzant funcions de Resampling (descartades al final per no millora)
* Aplicació de diversos models.
### Preprocessat
* Comprovació de valors nulls i duplicats. No ha afectat al resultat.
* Subsampling del dataset. Ha afectat en gran mesura ja que el dataset és enorme i la les categories estan desbalancejades.
* Obtenció de paraules clau de les URL. Ha ajudat molt als models per aprende i obtenir millor presició.
### Model
| Model | Hiperparametres | Accuracy | Temps |
| -- | -- | -- | -- |
| Logistic Regression | C:0.01 penalty:'l2' tol:0.001 | 37% | Baix(minuts) |
| Naive Bayes |  | 59% | Molt Baix(segons) |
| SVM | kernel: lineal C:0.1 gamma:0.9 | 42% | Molt alt(hores) |
| KNN | C=0.01, penalty='l2', tol=0.001 | 36% | Alt(hores) |
## Demo
Per tal de fer una prova, es pot fer servir amb la següent comanda
``` python3 demo/demo_url.py `
## Conclusions
El millor model que s'ha aconseguit ha estat el Naive Bayes.
#### Procés
* Hem vist com manipular i visualitzar les dades d'un dataset.
* Hem pre-processat les dades i hem extret les paraules clau de les URL.
* Hem afrontat un problema de desbalancejament de dades amb mètodes de Subsampling de les classes majoritàries.
  * S'han tingut problemes de memòria per processar tot el dataset ja que el seu tamany és enorme (+1.5 Millions d'instancies).
* Hem seleccionat, executat i comparat diversos models per un problema de classificació. 
  * D'aquests el més precís ha sigut el model Naive Bayes.
* Per últim hem treballat més a fons el model Naive Bayes i hem visualitzat les curves ROC i PCR d'una execució.
  * En aquestes curves, en general, hem obtingut un àrea propera a 1.

## Idees per treballar en un futur
* Com ha molt s'ha arribat a obtenir un 59% d'accuracy en el Naive Bayes. Això podria significar que o necessitem més dades de cada categoria o que en el procés d'obtenció de paraules clau s'haurien d'obtenir paraules encara més precises. 
* També es podria obtenir millors resultats modificant alguns hyperparàmetres dels models amb menys presició obtingunda o fer un resampling de totta la base de dades diferent a l'utilitzat.
## Llicencia
El projecte s’ha desenvolupat sota cap llicència.

