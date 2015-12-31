### IPTWeather\_20100509 ###
- L'option IPTWiPhoneTodayDisabled=-1 fonctionne désormais comme attendu (voir le fichier weather.ini pour plus d'informations)
- Les icônes météo d'iPhoneToday sont désormais toutes mises à jour, même si les icônes des prévisions météos sont affichées, ce qui permet d'avoir une page d'iPhoneToday dédiée pour les prévisions météos, sans avoir à les afficher/masquer

### IPTWeather\_20100429 ###
- Contournement d'un problème d'iPhoneToday afin de garantir que le fichier icons.xml avec les icônes originales de l'utilisateur ne soit pas modifié avec les prévisions météo. Le problème est que si des icônes temporaires sont définies avec la fonctionnalité reloadIcon=1 (icônes de prévision météo), alors, si on ajoute une icône avec le mode reloadIcon=2 afin d'écrire cette nouvelle icône dans le fichier icons.xml (icône de la météo actuelle), toutes les icônes temporaires sont aussi écrites dans le fichier icons.xml et non pas seulement celle définie avec le mode reloadIcon=2

### IPTWeather\_20100428 ###
- Ajout de l'option IPTWiPhoneTodayDisabled=-1 afin qu'IPTWeather ne désactive pas les mises à jour des icônes iPhoneToday automatiquement
- L'heure de mise à jour des données est comparée en heure locale afin que les données affichées soient les bonnes même lorsque l'on récupère la météo d'un autre fuseau horaire que le sien
- Lorsque IPTWupdateWeatherNowQuestion était vide, une mise à jour des données avait lieu systématiquement lorsque l'on masquait les prévisions météo, au lieu de ne le faire que si les données étaient plus anciennes que la durée définie par IPTWforceDelayHours et IPTWforceDelayMinutes.
- Nettoyage de code

### IPTWeather\_20100425 ###
- Paramètre pour l'icône météo de S2U2 automatiquement mis à UserWeather 05 si IPTWtomorrowForecastInS2U2UserWeather = 1 ou IPTWtomorrowForecastInS2U2UserWeather = -1
- Création du raccourci en mode écrasement lors de l'exécution du script autostartIPTWeather.mscr
- Ajout de l'option IPTWreloadLastDataOnStart=-1 (par défaut) pour que IPTWeather ne recharge pas les icônes au démarrage, puisque ce n'est plus utile avec les dernières version d'iPhoneToday grâce à l'option reloadIcon=2. Ceci permet notamment d'éviter le bug des versions 1.5.1 et 1.5.2 de iPhoneToday qui ne lit pas les valeurs de registre au démarrage.
- Ajout du script waitForReadyIPT.mscr pour une maintenance du code plus facile.
- Ajout d'un timer dans la mise à jour des valeurs de registre de iPhoneToday afin d'éviter qu'IPTWeather ne rentre dans une boucle infinie en cas de bug d'iPhoneToday.

### IPTWeather\_20100423 ###
- Désactivation automatique des mises à jour des icônes météo dans iPhoneToday si ce dernier n'est pas utilisé.
- Contournement d'un problème dans la version 1.5.2 de iPhoneToday qui ne contrôle pas la valeur de registre reloadIcons au démarrage.

### IPTWeather\_20100422 ###
- Plus de question pour mettre à jour la météo lorsque l'on change de ville, si IPTWupdateWeatherNowQuestion est vide.
- Ajout du paramètre IPTWS2U2UserWeatherIconToForce
- Ajout des options IPTWtodayForecastInS2U2Wallpaper=-1 et IPTWtodayForecastInS2U2Text=-1 pour montrer la météo actuelle dans le fond d'écran de S2U2 et/ou le "slide texte".
- Le fichier weather.ini installé par défaut utilise les fonds d'écran AccuWeather HD pourS2U2.

### IPTWeather\_20100414 ###
- Optimisation du code.
- Ajout de %HUM% pour le paramètre IPTWS2U2UserWeatherTextPattern pour montrer l'humidité actuelle.
- Correction de l'affichage du lieu courant affiché lors de l'appel du script manageIPTWLocation.mscr.
- Temps de "sleep" réduits pour une mise à jour plus rapide des icônes dans iPhoneToday.
- Ajout du ShowWaitCursor lors de l'exécution du script iPhoneTodayAccuWeather.mscr.
- Nouveau script userScriptOnUpdate.mscr. Il s'agit d'une sorte d'API qui s'exécute à chaque rafraîchissement de l'affichage de la météo afin de permettre l'exécution de scripts utilisateurs quelconques (par exemple pour déclencher un son lors de la mise à jour de la météo, etc.).
- Projet déplacé sur Google Code.
- Ajout du support de l'application Modaco App-to-date.

### IPTWeather\_20100401 ###
- Si IPTWgoToAccuWeatherQuestion est vide, alors la mise à jour de la météo est forcée sans poser de question.
- Ajout du champ %TXT% pour le paramètre IPTWS2U2UserWeatherTextPattern afin d'afficher la description de la météo sous l'icône du UserWeather de S2U2.
- Lorsqu'il est minuit passé, avec IPTWtomorrowForecastInS2U2UserWeather=-1, et sans données à jour, la météo de la nuit est affichée dans le UserWeather de S2U2 au lieu de la météo actuelle de la veille.

### IPTWeather\_20100330b ###
- Ajout des champs suivants pour le paramètre IPTWS2U2UserWeatherTextPattern : %CITY%, %SUNS%, %SUNR%, %OBSD% and %OBST%. Merci de se réferrer au fichier weather.ini pour la description de chaque champ.

### IPTWeather\_20100330 ###
- En mettant IPTWtomorrowForecastInS2U2UserWeather=-1, vous aurez dans S2U2 les conditions météos actuelles, et sous l'icône, les températures actuelles et du jour
- Ajout du paramètre IPTWS2U2UserWeatherTextPattern afin de définir un pattern pour le texte affiché sous l'icône météo de S2U2. Merci de lire le fichier weather.ini pour plus d'information. Par défaut, ce paramètre est configuré de façon à afficher les informations relatives à l'activation de IPTWtomorrowForecastInS2U2UserWeather=-1.

### IPTWeather\_20100328 ###
- Vérification de l'existence de S2U2 lorsque IPTWtomorrowForecastInS2U2UserWeather=0 ou IPTWtodayForecastInS2U2Wallpaper=0 ou IPTWtodayForecastInS2U2Text=0 pour éviter les erreurs liées à une mauvaise configuration du fichier weather.ini par l'utilisateur
- Déplacement des scripts non-utilisateur utilisés par IPTWeather dans le répertoire sys
- Procédure de changement de chemin d'installation de IPTWeather simplifiée en supprimant l'étape 2 - changer le chemin d'IPTWeather dans la 3ème ligne du fichier config.xml", et remplaçant l'étape "1 - changer le chemin d'IPTWeather dans la 1ère ligne du script startAccuWeather.mscr" par "1 - Exécuter le script autostartIPTWeather.mscr"

### IPTWeather\_20100323 ###
- Ajout du paramètre IPTWaccuWeatherAPI par défaut à rdona, pour le cas où AccuWeather déconnecterait l'API rdona comme cela été le cas pour l'API rainmeter...
- La détection de l'utilisation de la version exe ou dll d'iPhoneToday se fait désormais à l'aide de la valeur suivante de la base de registre et non pas par l'existence de la fenêtre iPhoneToday : HKLM\Software\Microsoft\Today\Items\iPhoneToday\Enabled
- Si IPTWquickLocationChangeSleepMsgTime n'est pas paramétré, alors le script quickIPTWFavoriteLocationChange.mscr défini le paramètre par défaut à 1.
- Suppression du paramètre IPTWiPhoneTodayPath : le chemin d'iPhoneToday est détecté automatiquement, donc IPTWeather est désormais compatible avec toutes les versions d'iPhoneToday sans aucun paramètre à changer

### IPTWeather\_20100322 ###
- Suppression du paramètre IPTWuseExeIPhoneToday : désormais IPTWeather détecte tout seul si c'est la version .exe ou .dll qui est utilisée.
- Le code 'My Location' ne se base plus sur l'adresse IP pour définir la géolocalisation, mais utilise le service Sleuth's myLocation Service
- Ajout d'un test pour éviter l'erreur "'\Program Files\S2U2\lang.ini' couldn't be opened" lorsque l'utilisateur a mal configuré IPTWeather
- Ajout du paramètre IPTWquickLocationChangeSleepMsgTime pour définir le nombre de secondes pendant lequel le message montrant le nouveau lieu s'affiche, lors de l'utilisation des scripts quickFavoriteLocationChange.mscr et setIPTWFavoriteLocation.mscr
- Optimisation pour iPhoneToday 1.5.0 et supérieures : utilisation de la fonctionnalité reloadIcon = 2 afin de mettre à jour le fichier icons.xml pour l'icône météo principale