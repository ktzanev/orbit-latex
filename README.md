# orbit-latex

Ce dépot donne un exemple comment on peut utiliser [orbit](https://github.com/gulien/orbit) pour générer et compiler des fichier latex à partit de divers sources de données en utilisant le [langage des modèles](https://golang.org/pkg/text/template/) (*template*) de [go](https://golang.org/) enrichie des fonctions de [Spring](http://masterminds.github.io/sprig/).

## description

Le fichier [orbit-playload.yaml](orbit-payload.yml) contient la référence vers les données à utiliser :

  - `config` se réfère à [configuration.toml](configuration.toml)
  - `diection` se réfère à [data/direction.yaml](data/direction.yaml)
  - `equipes` se réfère à [data/equipes.yaml](data/equipes.yaml)

Le fichier [rapport-template.tex](rapport-template.tex) est le modèle qui est transformé en `raport2019.tex`, en utilisant les données.

Le fichier [orbit.yml](orbit.yml) definit les commande executables par [orbit](https://github.com/gulien/orbit) :

 - `generate` (à évoquer avec `orbit run generate`) génère le rapport `raport2019.tex` à partir du modèle [rapport-template.tex](rapport-template.tex).
 - `compile` (à évoquer avec `orbit run compile`) compile le `raport2019.tex` en `raport2019.pdf`.
 - `all` (à évoquer avec `orbit run all`) génère, compile et affiche le résultats `raport2019.pdf`.

## utilisation

- dupliquer ce répo :
```
git clone https://github.com/ktzanev/orbit-latex.git
```
- télécharger l'executable d'orbit [pour vôtre platforme](https://github.com/gulien/orbit/releases) : c'est un fichier unique.
- mettre ce executable dans le répértoire `orbit-latex` contenant les sources de ce répo, où dans un autre répértoire de votre chemin d'accès.
- executer dans le répértoire `orbit-latex` la commande:
```
orbit run all
```
