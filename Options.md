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

[Le média controller](Gmc.md)
