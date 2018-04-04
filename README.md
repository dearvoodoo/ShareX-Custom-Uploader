# ShareX-Custom-Uploader
Script pour upload avec ShareX sur votre propre Hébergeur.

# Installation
Premièrement vous uploadez le contenue dans le 'src' de votre site.

Après on passe à la configuration du fichier upload.php. Il y a quelques informations à modifier.


Auto Destruction du fichier après 1 jour. Vous pouvez changer la valeur de '$days' ligne 4.
```
$days = 1;
```

Ligne 23 à 25 vous devez entrer vos informations d'upload.
```
$key = "TypeHereSomeRandomKeyOrPassword"; <-- Mettre un Mot de passe ou une Clé
$uploadhost = "http://example.com"; <-- Votre URL de host (url ou ce trouve le fichier upload.php)
$redirect = "http://example.com/"; <-- URL de redirection
```
# Configuration de ShareX 
Nous devons maintenant faire la configuration de ShareX pour votre Uploader
```
1. Directement depuis l'application ShareX aller à Destinations > Paramètres de destination...
2. Scroll en bas de la liste jusqu'à 'Services de mise en ligne personnalisés' et ajouté un nouveau profil
3. Type de requête POST, URL de la requête doit être http://www.example.com/upload.php
4. Nom de la forme du fichier: "form" (sans guillemets)
5. Arguments:
    - user, c'est ici que vous devez mettre la clé inscrite plus tôt dans le fichier upload.php
6. La configuration est terminée, tester votre uploader
```
![Aperçu en image de la configuration de ShareX](https://imgur.com/WAktc05)

# Aperçu de Directory Lister
![Aperçu Directory Lister](https://imgur.com/3XGMIrt)
![Directory Lister](http://www.directorylister.com)
