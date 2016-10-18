# Lier serveur-site

<aside class="alert alert-warning">
  <h3>Compatibilité</h3>
  <p>Les plugins sont compatibles à partir de la version 1.7.10</p>
  <p><small><em>Des problèmes de compatibilités peuvent survenir avec Cauldron.</em></small></p>
</aside>
<aside class="alert alert-info">
  <p><strong>Type de connexion</strong>:  <br>
  - Par défaut : <em>Connexion à un serveur lié avec le <a href="http://mineweb.org/dl/plugin/bukkit/last">plugin Bukkit/Spigot</a>, permet l’utilisation de toutes les fonctionnalités du CMS (Boutique, Classement factions, Vote…)</em> <br>
  - BungeeCord : <em>Connexion à un serveur lié avec le <a href="http://mineweb.org/plugin_bungee/1.0.3-mineweb_bungee.jar">plugin BungeeCord</a>, permet l’utilisation de <strong>certaines fonctionnalités</strong> (affichage des joueurs, commandes, mais la <strong>boutique</strong> et le <strong>classement</strong> factions <strong>ne pourront pas être utilisés</strong> avec ce type de connexion)</em> <br>
  - Ping : <em>Connexion à un serveur sans plugin, permet uniquement d’avoir le nombre de joueurs en ligne et le nombre de joueurs maximums (La <strong>boutique</strong> et le <strong>classement</strong> factions <strong>ne pourront pas être utilisés</strong> avec ce type de connexion) </em></p>
</aside>

## Configuration préalable

Rendez-vous sur la page de liaison site-serveur sur le panel admin de votre CMS.
Vous devez dans un premier temps configurer le temps d’exécution maximum (appelé aussi timeout), il est conseillé de mettre 1 (secondes).

![](http://pic.eywek.fr/491537.png)

<aside class="alert alert-info">
Vous avez a côté 2 boutons pour désactiver la fonctionnalité (mettra automatiquement le statut du serveur à éteint) si vous ne souhaiter pas utiliser la liaison site-serveur. Et un autre bouton pour activer/désactiver le cache sur la “bannière” (Permet que le message affiché sur le site (joueurs connectés, MOTD…) soit stocké pendant quelques minutes permettant d’éviter la surcharge de commande au serveur)
</aside>

## Liaison à un serveur Bukkit/Spigot

Maintenant nous allons lier votre __serveur Minecraft__ au __CMS__. Pour cela vous devez avoir installé sur votre serveur le plugin MineWeb disponible à [cette adresse](http://mineweb.org/dl/plugin/bukkit/last).
Une fois le plugin téléchargé, placez-le dans votre dossier plugins de votre serveur et __redémarrez celui-ci__.
Vous n’avez __pas à toucher à la configuration du plugin__.
Quand votre serveur est en ligne, configurez le port que va utiliser le plugin pour communiquer avec le site, pour cela tapez la commande `/mineweb port PORT` en remplaçant bien sur __PORT__ par un port __disponible__, __non utilisé__ et __ouvert__.

<aside class="alert alert-info">
Si vous ne savez pas quel port utiliser, demandez à votre hébergeur minecraft quels ports sont disponibles. Si vous utilisez un Dédié ou un VPS, essayez par exemple des ports comme 4343 ou ou 26178.
</aside>

Une fois que cette commande est effectuée tapez `/mineweb setup`. Et rendez-vous sur la page de liaison site-serveur dans le panel admin.

Maintenant que vous avez configuré le serveur vous pouvez __ajouter un serveur__ et remplir les informations nécessaires :

- Type de la connexion, donc mettez _Par défaut_.
- Nom par le nom affiché.
- IP par l’ip (ou domaine) sans le port.
- Port configuré par le port que vous avez tapé juste avant.

Cliquez ensuite sur Connexion pour tester la connexion, si celle-ci échoue, votre __port n’est pas ouvert__ ou __non disponible__.

## Liaison à un serveur BungeeCord

Même processus que pour la liaison Bukkit/Spigot mais avec le [plugin BungeeCord](http://mineweb.org/plugin_bungee/1.0.3-mineweb_bungee.jar) et vous devez mettre comme type de connexion _Bungeecord_.

## Liaison par Ping

Vous n’avez pas besoin de plugin pour cette liaison, il vous suffit juste de configurer un serveur comme ceci depuis la page de liaison :

- Type de la connexion, donc mettez _Ping_.
- Nom par le nom affiché.
- IP par l’ip (ou domaine) __sans le port__.
- Port de votre serveur (25565 par défaut si vous n’avez pas de port).

Cliquez ensuite sur _Connexion_ pour tester la connexion.

## La connexion échoue

Dans un premier temps, vérifiez que vous n'avez pas d'__erreur dans la console__ de votre serveur en rapport avec le plugin MineWeb.

Dans un second temps, vérifiez que le __port__ que vous avez configuré est __ouvert__ et __non utilisé__ (demandez à votre hébergeur minecraft si vous ne savez pas lequel utiliser).

Ensuite, essayez de __redémarrer votre serveur__ juste après avoir fait les commandes, puis testez la connexion à nouveau.

Si la connexion échoue toujours, contactez le [support](http://mineweb.org/support) avec un maximum d'explications et d'informations, et répondez à ces questions :

- Quelle IP avez-vous mis ?
- Quel port ?
- Comment êtes-vous sûr que le port est ouvert ?
- Avez-vous fait toutes les commandes indiquées dans la doc ?
- Aucune erreur dans la console ?
- Avez-vous essayé de rédemarrer le serveur après avoir fait les commandes ?