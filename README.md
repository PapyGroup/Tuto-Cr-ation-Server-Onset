# Tuto-Creation-Server-Onset


[TUTO] Faire un serv Onset avec Mtx


Se référer à la vidéo suivante : 


https://youtu.be/jkyBy3uDRq4


Etape 1 Prérequis à télécharger :

-> onsetrp
-> dialogui
-> i18n
-> soundstreamer   --> améliore les communications
-> cinematicui    --> Cinématique avec PNJ
-> salsi    --> animation comme détécteur d'armes
-> onsetworld --> fix bugs map


Etape 2 : Injection BDD

-> Prendre le fichier /onset/packages/onsetrp Injecter roleplay.sql

Etape 3 : Liaison BDD

-> Aller dans -> /onset/packages/onsetrp/misc 
Modifier s-database.lua 

ATTENTION dans la base enlever le ".dist" sinon marche pas !

Ensuite compléter les champs.

Etape 4 : Starter les packages

-> Aller dans server_config.json

Start ---> plugins": [
		"mariadb",
		"ini-plugin"      ----> NE PAS OUBLIER CELUI CI SI MANQUANT
	],
	"packages": [
		"soundstreamer",
		"i18n",
		"dialogui",
		"cinematicui",
		"onsetrp",
		"salsi",
		"onsetworld"
	],

Attention aux virgules et à l'ordre des starts !!

Etape 5 : Fix problème de HUD 

--> aller dans -> /onset/packages/onsetrp/shops et ensuite dans client.lua
Modifier ceci --Dialog.setGlobalTheme("onset")-- par --Dialog.setGlobalTheme("flat")--


Tuto écrit tous droits réservés. Papy Group / Papy Brossard - Alexis Brossard
