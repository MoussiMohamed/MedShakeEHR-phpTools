# MedShakeEHR-phpTools
Outils PHP pour MedShakeEHR

/cli/
- importVillagePeople.php : 
    - dans un contexte de démo à ne pas utiliser sur une installation existante.
    - importer le CSV obtenu via le script [MedShake Village People](https://github.com/MedShake/VillagePeople) à la racine de l'installation.
    - supprimer la ou les lignes d'utilisateur ou de patient déjà configurés `awk -F, '$1 != 5' export.csv > export_5.csv && mv export_5.csv export.csv`.
    - copier le dossier cli à la racine de l'installation.
    - modifier les occurences `setFromID('5');` avec le numéro de l'utilisateur souhaité.
    - lancer la commande `php cli/importVillagePeople.php`, ne pas toucher au logiciel jusqu'à la fin de l'opération.


/web/
- diagnostic.php : script de diagnostic de problèmes courants. Placer dans public_html et accéder par navigateur.   
