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
| Model | Hiperparametres | Mètrica | Temps |
| -- | -- | -- | -- |
| [Random Forest](link) | 100 Trees, XX | 57% | 100ms |
| Random Forest | 1000 Trees, XX | 58% | 1000ms |
| SVM | kernel: lineal C:10 | 58% | 200ms |
| -- | -- | -- | -- |
| [model de XXX](link al kaggle) | XXX | 58% | ?ms |
| [model de XXX](link al kaggle) | XXX | 62% | ?ms |
## Demo
Per tal de fer una prova, es pot fer servir amb la següent comanda
``` python3 demo/demo.py --input here ```
## Conclusions
El millor model que s'ha aconseguit ha estat...
En comparació amb l'estat de l'art i els altres treballs que hem analitzat....
## Idees per treballar en un futur
Crec que seria interesant indagar més en...
## Llicencia
El projecte s’ha desenvolupat sota llicència ZZZz.

