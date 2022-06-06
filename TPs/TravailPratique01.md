# Travail pratique 1 - Procédure d'installation d'un serveur

**But :** le but de ce laboratoire est de **documenter** la procédure d'installation d'un serveur Ubuntu 22.04 LTS dans votre environnement de test.  **Attention documenter n'est pas installer**

   - Ce serveur doit utilisé un système de stockage LVM.
   - IL a carte réseau présente sur le réseau 10.100.2.0/24
   - Il y 2 processeur et 4 Go de mémoire vive.
   - Ce serveur devrait pouvoir être accédé depuis une machine client depuis le protocole ssh. 
   - Il faut que le service ssh soit sécurisé.
   - Il devrait être prêt à servir de modèle pour le déploiement de services supplémentaires.

## Voici les sections qui doivent être incluses dans votre procédure:

1. Caractérisation de la machine serveur :
   - Nom de la Vm et Nom de la machine (hostname)
   - Adresses IPv4, IPv6 (réseau) avec les informations de masque et de passerelle.
   - Fichier Hosts (partie liée à l'installation) 
   - Port des services ouverts.
   - Usager utilisé pour l'installation, autre que root.

2. Les mises à jour préalables à l'installation et ajout de composants nécessaires.
   Que doit contenir votre serveur pour devenir un modèle de déploiment.
   - Programmes : Nom, version, procédure d'installation.
   - Répertoire utilisé pour le programme, ses fichiers de configuration, ses données.
   - Espace utilisé et droits sur les répertoires.
   - Nom d'usager (UID) et groupe (GID) pour le programme au sein du système et dans l'application.
   - Liste des commandes nécessaires pouvant être exécutées par une tierce personne.
   - Exemple 
      - SSHD
      - update
      - upgrade

4. Procédure de validation de l'installation.

   Cette procédure utilisée par une tierce personne devrait démontrer le bon fonctionnent du serveur et comprendre les commandes nécessaires à la vérification des caractéristiques du serveur.


## Vous devez fournir :

- Un dépôt GitHub de votre travail

    - Attention ce dépôt doit être privé
    - Le professeur doit être collaborateur ainsi que les 2 membres de l'équipe
    - Un fichier readme.md qui résume les informations sur le dépôt
         - Date 
         - Membre de l'équipe
         - Contexte
- Votre fichier avec toutes les parties demandées. Vous devez utiliser le format Markdown (md).
- Vous devez utiliser des images pour favoriser la compréhension.
- Vous devez donner vos sites de références.

## Consignes :

- Le temps  alloué en classe est de trois (3) périodes de 1 heure pour un total de trois (3) heures.
- La date de remise est celle indiqué sur LÉA.
- Ce travail pratique vaut pour 10 % de la note finale.
- Ce travail est réalisé en équipe de 2 membres et seuls les membres de cette équipe y contribuent.
- Tout le matériel est autorisé.
- Toute copie de code, de portion de code, d’algorithme ou de texte doit faire mention de sa source.
- Tout constat de plagiat, tricherie ou fraude sera automatiquement déclaré à la Direction et les sanctions prévues seront appliquées.


## Références à consulter :

- Installation  : https://ubuntu.com/tutorials/install-ubuntu-server#1-overview
- Markdown : https://guides.github.com/features/mastering-markdown/
- Notes de cours et exercices : https://github.com/jpduchesneauCegep/420-W44-SF-4393


## Évaluation :
|Item |Points  |
--- | --- | 
|Dépôt GitHub |20|
|Respect des caractérisitique |20|
|Mise à jour préalable  |30|
|Procédure de vérification |30|
|Total|100