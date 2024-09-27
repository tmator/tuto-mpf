# Options

Nous verrons ici, comment configurer certains éléments spécifiques (autofire, drop target,...) ainsi que des options utiles sur des éléments que nous avons déja configuré.

## Les bobines

Il y a beaucoup de paramètres que l'on peut passer sur les [bobines}(https://missionpinball.org/latest/config/coils/), voici quelques paramètres utiles.

Quand on met allow_enable: true sur une bobine, cela signifique que l'on poura maintenir cette bobine à l'état actif; pour les bobines de maintien sur les batteurs par example.

Le paramètre default_pulse_ms: 20 permet de dire combien de temps on souhaite activer la bobine, par défaut c'est 10ms mais il est souvent necessaire de jouer avec ce paramètre pour que les bobines fonctionnent correctement.

## Les cibles tombantes (Drop Target)

Voic un exemple ou l'on défini un lot de cibles tombantes. Dans la section drop_targets on défini les switchs qui sont associé aux cibles. 
Dans la section drop_target_banks on définie les actions qui remettent à zéro le lot de cible ne précisent les cibles définies précédement, la bobine qui les remonte et au bout de combien detemps.


	drop_targets:
    		#alpha2
    		a2_1_drop_target:
      			switch: s_alpha_2_target_1
    		a2_2_drop_target:
      			switch: s_alpha_2_target_2
  
  	drop_target_banks:
    		#alpha2 reset
    		alpha2_drop_targets:
      			drop_targets: a2_1_drop_target, a2_2_drop_target
      			reset_coils: c_2
      			reset_on_complete: 1s

## L'autofire

Il arrive parfois que l'on ai besoin de définir des déclemchement de bobine automatique, comme pour les slinshot, bumpers...

Voici un exemple dans lequel on dit que lors de l'activation du switch s_left_slingshot on activera la bobine c_left_slingshot :

  	autofire_coils:
    		left_slingshot:
      			coil: c_left_slingshot
      			switch: s_left_slingshot

## Ajouter un "hook"

Vous pouvez ajouter du code Python pour effectuer des action spéciales ou complexe à gérer avec mpf. Dans l'exmple ci-dessous nous alons voir comment activer deux bobines en même temps. Pour commencer il faut créer un dossier code à la racine du projet dans lequel nous créeron un fichier vide __init__.py et un fichier python qui contiendra le code 2bobine.py.

Voici un exmple de code qui active deux bobines simultanément.

	from mpf.core.custom_code import CustomCode


	class 2Bobine(CustomCode):

 	#cette fonction est activé au lancement
    	def on_load(self):

        	#si la bille est présente sur le switch1 plus de 100ms, on appelle la fonction qui active deux bobines
        	self.machine.switch_controller.add_switch_handler('s_1', self.active2, ms=100)

	#cette fonctione active deux bobines, la première étant un relai dans mon cas
    	def active2(self):

        	self.machine.coils['c_relay_s'].pulse(pulse_ms=100)
        	self.machine.coils['c_4'].pulse(pulse_ms=20)

Pour activer ce conde, il faut le préciser dans le config.yaml :

	custom_code:
  		- code.2bobine.2Bobine

Il y a bien sur tout un tas de fonctions et paramètres accéssibles dans la doc de référence : https://missionpinball.org/latest/code/api_reference/

[Le média controller](Gmc.md)
