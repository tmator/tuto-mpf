# Choix du hardware

Pour faire fonctionner le flipper il faut une carte compatible avec MPF qui fera l'interface entre le PC et le hardware.

## Flipper existant
 
Voici une liste non exhaustive des solutions permettant de gérer certains systèmes existants.

**Bally/Stern AS-2518-17 ou AS-2518-35**
 
 Ces machines peuvent être gérées avec les cartes Lisy 35	https://lisy.dev/

 Definition de la plateforme dans le fichier de configuration :

 	hardware:
  		platform: lisy
	lisy:
  		connection: serial
  		port: com1               # replace this with your com port
  		baud: 115200
	 
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

[Installation](Installation.md)
