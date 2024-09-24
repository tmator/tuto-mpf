# Godot Media Controller (GMC)

Cette partie est valable pour tous les systèmes sauf le Raspberry qui n'est pas assez puissant pour le GMC.

Le Media Controller. MPF-MC est une application distincte mais complémentaire à MPF, utilisée pour gérer tout ce qui concerne les médias, comme les animations, les sons, les vidéos et les effets visuels. Tandis que MPF contrôle la logique du jeu de flipper (détection des billes, action des bobines, etc.), MPF-MC se concentre sur la partie visuelle et sonore, permettant d'enrichir l'expérience de jeu.

Depuis la version 0.80, MPF utilise un nouveau média center qui utilise le moteur de jeu open source Godot qui permet de décupler les possibilités offertes au niveau visuel.
Godot utilise GDScript, un langage de programmation simple et léger, similaire à Python, spécialement conçu pour être facile à apprendre et à utiliser dans le développement de jeux.

## Installer Godot et configurer le GMC

Pour commencer il faut télécharger Godoot et le décompresser dans un dossier (en dehors du dossier de votre jeu).

Lancez ensuite Godot, puis créer un projet en sélectionnant comme dossier le dossier de votre projet MPF (attention à décocher la case créer un dossier), entrez un nom pour votre projet et choisissez le moteur de rendu. Dans la majorité des cas, le moteur "Mobile" est suffisant.

Maintenant, vous pouvez télécharger le plugin GMC à partir du dépôt MPF-GMC sur GitHub. Rendez-vous sur https://github.com/missionpinball/mpf-gmc et cliquez sur le bouton vert 'Code' pour afficher le menu déroulant 'Code', puis sélectionnez 'Download ZIP' pour télécharger le plugin.

Extrayez le fichier ZIP téléchargé et copiez le dossier addons dans le répertoire de votre projet.

Dans Godot, allez dans Projet->Pramètres du projet, puis sur l'ognlet extensions et Activez "Godot MC".

Ensuite dans l'onglet Généraux->Chargement automatique

Enregistrez le projet et relancez Godot.
