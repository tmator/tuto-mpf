# Choix du hardware

Pour faire fonctionner le flipper il faut une carte compatible avec MPF qui fera l'interface entre le PC et le hardware.

## Flipper existant
 
Voici une liste non exhaustive des solutions permettant de gérer certains systèmes existants. Vous trouverez au bas de cette page les cdéfinition des différentes plateformes à mettre dans le fichier conig.yaml.

**Bally/Stern AS-2518-17 ou AS-2518-35**
 
 Ces machines peuvent être gérées avec les cartes Lisy 35	https://lisy.dev/
	 
**Gottlieb System 1 et System 80**
	
Ces machines peuvent être gérées avec les cartes Lisy 1 et Lisy 80	https://lisy.dev/

**Williams System 3 à 9**
	 
Ces machines peuvent être gérées avec les Arduino Pinball Controller (APC) https://github.com/AmokSolderer/APC via le protocole Lisy 



 **Williams, Bally System 11**
 
Ces machines peuvent être gérées avec :
	 
 - L'Arduino Pinball Controller (APC) https://github.com/AmokSolderer/APC via le protocole Lisy 
 - La solution FAST Retro https://fastpinball.com/retro/system-11/
 - La carteP-ROC avec une carte driver SNUX https://www.multimorphic.com/store/circuit-boards/p-roc/

**Data East**

Ces machines peuvent être gérées avec les Arduino Pinball Controller (APC) https://github.com/AmokSolderer/APC via le protocole Lisy 

**Sega/Stern Whitestar**

Ces machines peuvent être gérées avec la carte P-ROC https://www.multimorphic.com/store/circuit-boards/p-roc/

**Stern SAM**

Ces machines peuvent être gérées avec la carte P-ROC https://www.multimorphic.com/store/circuit-boards/p-roc/

**WPC, WPC-S, and WPC-95**

Ces machines peuvent être gérées avec :
	 
 - La solution FAST Retro https://fastpinball.com/retro/
 - La carte P-ROC avec une https://www.multimorphic.com/store/circuit-boards/p-roc/

**Pinball 2000**

Ces machines peuvent être gérées avec la carte P-ROC https://www.multimorphic.com/store/circuit-boards/p-roc/

**Stern SPIKE/SPIKE 2**

Les contrôleurs SPIKE sont directement accessibles via USB.

## Flipper maison
 
Voici quelques solutions matérielles pour gérer son flipper :

 - CobraPIN https://pinballmakers.com/wiki/index.php?title=CobraPin
 - OPP https://pinballmakers.com/wiki/index.php?title=OPP
 - P-ROC et P3-ROC https://www.multimorphic.com/store/circuit-boards/p3-roc/
 - Fast Pinball https://fastpinball.com/products/
 - Pinball PKONE https://www.pennykpinball.com/


 Definition des plateformes Lisy et APC :

 	hardware:
  		platform: lisy
	lisy:
  		connection: serial
  		port: com1               # replace this with your com port
  		baud: 115200


Definition de la plateformes Fast :

 	hardware:
  		platform: fast
	fast:
    		ports: com3, com4, com5               # replace this with your com port


Definition de la plateformes OPP / CobraPin :

 	hardware:
  		platform: OPP
	opp:
  		port: com1               # replace this with your com port


Definition des plateformes P-ROC ou P3-ROC :

 	hardware:
  		platform: p_roc #ou  p3_roc
	p_roc:
  		driverboards: pdb


Definition des plateformes SPIKE/SPIKE2 :

 	hardware:
  		platform: spike
	spike:
  		port: /dev/ttyUSB0	# replace this with your com port
  		baud: 115200
  		flow_control: false
  		debug: false
  		nodes: 0, 1, 8, 9, 10, 11   #a définir suivant le jeu
  		runtime_baud: 115200


Definition de la plateformes pkone :

 	hardware:
  		platform: pkone
	pkone:
   		port: com3  # replace this with your com port



[Installation](Installation.md)
