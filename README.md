# Challenge 48h

***Groupe 7*** : Antoine Delbrel, Antoine Durand, Emma Durand, Hugo Marques et Lucas Mouchague.

***Diapo*** : [Challenge48h.pdf](Challenge48h.pdf)

___

***La problématique :***
- La communication interne dans une entreprise est très importante, sans elle il est très probablement impossible de faire grandir une entreprise dû au manque de lien professionnel / social entre les salariés. L'importance de cette communication interne est commune à tout les groupes sociaux / professionnel, elle l'est donc aussi au sein d'association. Le problème étant que, bien souvent, les associations n'ont pas les moyens de financer la mise en place et le maintient de logiciel professionnel pouvant améliorer la qualité de communication et donc de production entre les membres.
- C'est pourquoi nous devons donc trouver un moyen de fournir les mêmes services pour une association que pour une entreprise, le but final étant de pouvoir fournir ces services gratuitement aux associations tout en restant rentable.
- Comment améliorer la communication interne des associations, tout en conservant une offre gratuite pour ces derniers ?

___

***Solution :***

* Mise en place d’une suite de services et d’outils de productivité :

1. Traefik :
    - edge router (routing, reverse proxy)
    - open source (gratuit), utilisé à grande échelle en entreprise, facile d'utilisation
2. Hébergement de site
    - NextCloud :
        - Plateforme de partage fichier (style googledrive) permettant de travailler à plusieur sur le même fichier, gestionnaire planning, agenda, appel visio-conférence ...
        - Déjà connu par les membres de l'équipe, utilisé dans le milieu pro, open source (gratuit), facile à mettre en place, maj régulière, extensible ...
    - Rocket.chat :
        - Messagerie instantané avec plusieurs serveurs de discussion pouvant être composé de différents cannaux écrit
        - Open source (gratuit), déjà connu des membres de l'équipe, extensible ...
    - Mastodon :
        - Réseaux social pour faire communiquer / partager les assos avec leurs volontaires
        - Open source (gratuit), assez reconnu / utilisé, l'un des seuls logiciel à faire un bon réseau social
    - BookStack :
        - Documentation communautaire pouvant être utilisé par les assos pour partager leur savoir (administratif / logistique / etc)
        - Open source (gratuit), connu des membres de l'équipe, facile d'utilisation
    - MailCow :
        - Service de mail (envoi, réception)
        - Open source (gratuit), utilisé en entreprise, facilement déployable, existe depuis longtemps et régulièrement maj

___

### Business plan de notre startup

#### Pack startup :

- Installation de toute la stack chez nous 599,99€ HT avec infogérance à 60€/h
- Installation chez eux 459,99€ HT avec infogérance à 60€/h


#### Pack entreprise :

- Installation de toute la stack chez nous 5999,99€ HT avec infogérance à 85€/h
- Installation de toute la stack chez eux 4599,99€ HT avec infogérance à 85€/h

#### Pack association :

- FREE
- Préciser dans le contrat que les données personnelles ne sont pas stockées sur le serveur.
- Suite d'outils.

___

### Exemple de prototypage

Association : commentfairedu.biz

- Déployer sur Homer ou Heimdall : http://bigmacavecceci.commentfairedu.biz:15000/

**Outils :**
* NextCloud : http://nextcloud.commentfairedu.biz:15000/
  * administrateur : nawak / Toortoor1234!
* RocketChat : http://chat.commentfairedu.biz:15000/
  * administrateur : challenge / toortoor
  * utilisateur : créer un compte
* Mastodon :
  * cred : challenge@gmail.com / toortoor
  * cred : antoine@gmail.com / toortoor
* BookStack : http://book.commentfairedu.biz:15000
  * administrateur : admin@admin.com / password
  * utilisateur : jesuisendeficit@gmail.com / toortoor
* Serveur de mail : https://mail.commentfairedu.biz/

Pour la mise en place de la solution, nous avons utilisé docker-compose pour tout déployer. Nos fichiers de configuration sont : [ici](stack)
