# Atelier de tir

Une seule appli Android, hors ligne, en quatre parties reliées :

- **Recharge** : le Carnet de rechargement (séances, étuis, composants, résultats).
- **Tir** : le Carnet de tir (tirs, vitesses au chrono, munitions, armes et lunettes).
- **Clics** : le calcul des clics de tourelle (hauteur et vent) pour l'arme et la munition choisies.
- **GRT** : import des calculs de Gordon's Reloading Tool (export JSON). Chaque calcul crée sa fiche munition dans Tir (avec l'échelle de charges, vitesses et pressions prévues), sert de point de départ à une séance dans Recharge et fournit le coefficient G1 et la vitesse prévue à Clics.

Les trois parties partagent les mêmes données sur le téléphone. Dans une fiche munition du Carnet de tir,
le bouton « Calculer les clics avec cette munition » ouvre Clics avec le poids d'ogive, le coefficient G1
et la moyenne des vitesses mesurées au chrono.

## Installer ou mettre à jour
Onglet **Releases** du dépôt → **AtelierDeTir.apk** → ouvrir sur le téléphone.
Les mises à jour sont signées avec la même clé (`signature/`) et s'installent par-dessus sans perte de données.

## Récupérer les données des anciennes applis
Dans l'ancien Carnet de tir et l'ancien Carnet de rechargement : **Données → Exporter en JSON**.
Dans Atelier de tir, onglet correspondant : **Données → Importer une sauvegarde**.

## Fichiers
- `www/index.html` : la barre d'onglets.
- `www/tir.html`, `www/recharge.html`, `www/clics.html` : les trois parties.
- `.github/workflows/build-apk.yml` : construit et publie l'APK à chaque modification.
