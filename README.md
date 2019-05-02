# orbit-latex

Ce dépot donne un exemple comment on peut utiliser [orbit](https://github.com/gulien/orbit) pour générer et compiler des fichier latex à partit de divers sources de données en utilisant le [langage des modèles](https://golang.org/pkg/text/template/) (*template*) de [go](https://golang.org/) enrichie des fonctions de [Spring](http://masterminds.github.io/sprig/).

Le fichier `orbit-playload.yaml` contient la référence vers les données à utiliser :

  - `config` se réfère à `configuration.toml`
  - `diection` se réfère à `direction.yaml`
  - `quipes` se réfère à `equipes.yaml`

Le fichier `rapport-template.tex` est le modèle qui est transformé, en utilisant les données, en `raport2019.tex`.

Le fichier `orbit.yaml` definit les commande executables par [orbit](https://github.com/gulien/orbit) :

 - `generate` (à évoquer avec `orbit run generate`) génère le rapport `raport2019.tex` à partir du modèle `rapport-template.tex`.
 - `compile` (à évoquer avec `orbit run compile`) compile le `raport2019.tex` en `raport2019.pdf`.
 - `all` (à évoquer avec `orbit run all`) génère, compile et affiche le résultats `raport2019.pdf`.
