    # Configurer son flipper


## Créer la structure de dossier

Il faut en premier créer un dossier principal dans lequel nous créerons un dossier config pour stocker les fichiers de configuration de la machine.

J'utilise dans les exemples des informations venant d'un flipper Robowar de Gottlieb pour imager le tout.

## Créer les fichiers de configuration

MPF utilise des fichiers **YAML**. Les fichiers **YAML** (Yet Another Markup Language) sont des fichiers de configuration utilisés pour structurer des données de manière simple et lisible par les humains.

Le fichier nécessaire au fonctionnement de MPF est le fichier **config.yaml**, c'est lui qui contiendra la configuration de votre flipper. On peut tout mettre dans ce fichier, mais pour des raisons de lisibilité, il est préférable de créer plusieurs fichiers (un pour les switchs, un pour les bobines...). Nous allons donc créer les fichiers suivants dans le dossier config :

- config.yaml configuration principale
- switchs.yaml configuration des switchs
- coils.yaml configuration des bobines
- lamps.yaml configuration lampes

Nous ajouterons ensuite des fichiers en fonction des options du flipper (par exemple les afficheurs, les cibles tombantes...).

Pour éditer les fichiers YAML, un simple éditeur de texte suffit, mais un éditeur avancé comme VSCODE, Notepad++, atom ou autre vous apportera des options afin de faciliter la création de ceux-ci.

## La configuration

En premier lieu, il faut mettre au début de chaque fichier la directive suivante :

**#config_version=6**

Elle permet d'indiquer qu'une version de MPF > 0.57 est nécessaire pour exécuter cette machine.

Ensuite, il faut inclure tous les fichiers que nous avons créés dans le fichier config.yaml de cette façon :

    
    #config_version=6
    
	config:
     - switches.yaml
     - coils.yaml
     - lamps.yaml
     - nter config_version=6

Il faut maintenant définir dans chaque fichier les éléments du flipper.

Pour les lampes, on nomme chaque lampe (ex : l_shoot_again et on l'identifie, ici 3 car c'est la lampe 3 sur la matrice de lampe du flipper Robowar) :

	#config_version=6
	lights:
		  l_shoot_again:
		    number: 3
		  l_r:
		    number: 5 here


Pour les bobines, on nomme chaque bobine (ex : c_1 et on l'identifie, ici 1 car c'est la bobine 1 qui permet de remonter les cibles tombantes Alpha du flipper Robowar) :

	#config_version=6
	coils:	
	  c_1:
	    number: 1

Pour les switchs, on nomme chaque contact (ex : s_shooter_lane_rollover et on l'identifie, ici 36 car c'est le contact 36 de la matrice de switchs du flipper Robowar) :

	#config_version=6
	switches:	
	  s_shooter_lane_rollover:
	    number: 36

Il suffit de remplir les fichiers, et tous les éléments seront alors identifiés et prêts à être utilisés.

Vous trouverez ici les fichiers de Robowar avec les définitions de base.