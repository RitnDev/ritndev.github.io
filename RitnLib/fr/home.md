# Présentation
Ce mod est une bibliothèque de fonctions et depuis la version 0.7 elle ajoute surtout des classes utilisées dans la plupart des RitnMods. 
Vous pouvez évidement utiliser cette bibliothèque pour vos mods.

Il suffit d'ajouter ce mod comme dépendance.

## Settings stage
RitnLib n'ajoute actuellement aucune fonction pour cette étape du chargement de jeu.

## Data stage
Il existe des fonctions et classes pour cette étape du chargement de jeu.
Pour y avoir accès vous pouvez inclure le fichier de définition afin ensuite de chargé uniquement les modules que vous avez besoins.

```
-- INITIALIZE
---------------
if not ritnlib then require("__RitnLib__/defines") end
```

Ensuite, si vous avez par exemple besoin de la classe "RitnProtoRecipe" afin d'en utiliser les méthodes il vous suffit d'ajouter après la déclaration des définitions : 
```
local RitnProtoRecipe = require(ritnlib.defines.class.prototype.recipe)
```


la variable **ritnlib** est global à tous le Data stage, c'est à dire que vous pouvez y accédez depuis "data-updates.lua" si vous l'avez déclaré dans le fichier "data.lua".


Par contre, la variable (classe) **RitnProtoRecipe** est local au fichier où il est déclaré. Il est d'ailleurs préférable de toujours utiliser, autant que faire se peut, les variables locales. Ces dernières occupent moins de place en mémoire et sont plus rapides.