---
product: campaign
solution: Campaign
title: À propos de la gestion SFTP
description: En savoir plus sur la gestion SFTP dans le Panneau de contrôle
testing: SSECD-836 2
feature: Control Panel, SFTP Management
role: Admin
level: Intermediate
exl-id: b2c3be80-0d1b-4998-87ab-5280c6213f3d
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 100%

---

# À propos de la gestion SFTP {#about-sftp-management}

Dans le Panneau de contrôle, vous pouvez interagir avec tous les serveurs SFTP qui sont connectés aux instances Campaign auxquelles vous avez accès. Pour la plupart des instances, des serveurs SFTP sont connectés (dans certains cas, les instances de développement et de test peuvent ne pas être connectées à des serveurs SFTP).

L’accès aux serveurs SFTP est effectué à l’aide de logiciels clients SFTP que vous pouvez trouver et télécharger en ligne. Pour vous connecter à un serveur, que ce soit par le biais d’une application cliente ou d’une API, vous devez configurer une clé SSH publique et ajouter l’adresse IP qui se connecte à votre serveur SFTP à la liste autorisée.

Le Panneau de contrôle permet d’effectuer les actions suivantes pour gérer vos serveurs SFTP :

* surveiller leur **capacité de stockage** ;
* gérer **les listes autorisées d’adresses IP** : ajouter ou supprimer des plages d’adresses IP pour un ou plusieurs serveurs ;
* gérer les **clés SSH publiques** pour accéder à vos serveurs.

Des informations détaillées sur chacune de ces actions sont disponibles dans les sections ci-dessous.
