```
 ______________________________
< Test Jenkins sur le projet Cowsay >
 ------------------------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```

## Groupe

- THIEBAUT Mattéo 
- Pierre Legros
- baha akeem
- RANDRIANAINA Manoarijaona
- Vuylsteker Vincent

## Projet

On a choisi de partir avec le projet Cowsay.
Le principe était de lancer un package sur Jenkins en mode free style et en mode pipeline pour tester.
Ensuite on a remarqué que le package permet de tester si tous les fonctionnalités du projet fonctionne correctement.
Donc ensuite on a automatisé les tests avec le mode pipeline et le fichier Jenkinsfile pour faire un package et publier les artéfacts sur Jenkins.
Puis nous avons essayé avec le ficher jenkinsfile de relier Jenkins à nexus pour pousser les artéfacts sur un répository nexus.
Après de nombreux tests et de tutoriale suivie pour relier Jenkins et Nexus 3, nous avons presque reussi à relier les deux comme on peut le voir dans le fichier Jenkins File. Mais la plupart des tutoriels sont anglais comme la documentation donc compliquée de réussir à réparer une erreur présice.