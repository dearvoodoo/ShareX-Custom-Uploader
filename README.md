# ShareX-Custom-Uploader
Script pour upload avec ShareX sur votre propre Hébergeur.

# Installation
Premièrement vous uploadez le contenu dans le 'src' de votre site.

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
1. Directement depuis l'application ShareX aller à Destinations > Custom Uploader Settings...
2. Ajouté un nouveau profil
3. Type de requête POST, URL de la requête doit être http://www.example.com/upload.php
4. Nom de la forme du fichier: "form" (sans guillemets)
5. Body:
    - Body doit être sur "From data (multipart/form-data)"
    - Name doit être "user", et pour la valeur de user vous devez mettre la clé inscrite plus tôt dans le fichier upload.php
6. La configuration est terminée, tester votre uploader
```
![Aperçu en image de la configuration de ShareX](https://i.ibb.co/x7CGNnb/cu.png)

![Résultat d'un test positif pour un upload d'image](https://i.ibb.co/7r8nBFZ/cu-valid.png)

# Aperçu de Directory Lister
![Aperçu Directory Lister](https://i.imgur.com/3XGMIrt.png)
[Directory Lister](http://www.directorylister.com)
(Déjà dans le contenu)

Update le 26/07/2019 Compatible ShareX 12.4.1
