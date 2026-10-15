# Hawkins Library — Android

Application Android de bibliothèque personnelle avec interface sombre moderne, inspirée des applications vidéo et de lecture.

## Fonctions de cette première version
- Accueil, onglet vidéos, onglet lecture et réglages.
- Ouverture du dossier Google Drive fourni.
- Ajout manuel de liens vidéo, PDF, EPUB ou autres liens.
- Lecteur vidéo intégré pour les liens directs compatibles et aperçu intégré pour les fichiers Google Drive.
- Aperçu PDF Google Drive intégré.
- Les liens ajoutés sont sauvegardés localement sur l'appareil.

## Construire l'APK sans installer Android Studio
1. Crée un dépôt GitHub vide nommé `HawkinsLibrary`.
2. Envoie tous les fichiers de ce dossier à la racine du dépôt (y compris `.github`).
3. Ouvre l'onglet **Actions**. Le workflow **Build APK** compile le projet.
4. Ouvre la dernière exécution réussie et télécharge l'artefact `HawkinsLibrary-apk`.
5. Décompresse l'artefact : `app-debug.apk` est l'application à installer sur Android.

## Limites importantes
- Google Drive ne permet pas à une application de lister librement tous les fichiers d'un dossier sans intégration Drive API/OAuth. Cette version ouvre le dossier source et permet d'ajouter les liens individuellement.
- L'aperçu Drive est intégré dans l'application, mais certains fichiers peuvent demander une connexion Google ou les autorisations de partage appropriées.
- Les liens EPUB Drive sont enregistrés, mais un lecteur EPUB complet nécessitera une intégration EPUB dédiée et un accès direct au fichier. Cette version ne prétend pas offrir toutes les fonctions avancées d'un lecteur comme Lithium.
- Pour une future version complète, il faudra configurer Google Drive API et OAuth afin de parcourir le dossier automatiquement, puis intégrer un vrai moteur EPUB.

## Accès automatique au dossier Google Drive
Pour lister automatiquement les fichiers du dossier au lieu d'ajouter les liens un par un, il faut créer un projet Google Cloud, activer Google Drive API et configurer OAuth. Le dossier doit être accessible au compte connecté. Ne partage jamais ton mot de passe ni un jeton OAuth dans le dépôt.
