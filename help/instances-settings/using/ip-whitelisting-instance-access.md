---
title: Listes autorisées d’adresses IP
description: Découvrez comment ajouter des adresses IP à la liste autorisée dans le panneau de contrôle pour accéder aux instances
translation-type: tm+mt
source-git-commit: d8fe1c2e847fa25919f81bf0a4195de5ad0b2781
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 100%

---


# Listes autorisées d’adresses IP {#ip-whitelisting}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange"
>title="À propos des listes autorisées d’adresses IP"
>abstract="Ajoutez des adresses IP à la liste autorisée pour accéder à vos instances."
>additional-url="https://images-tv.adobe.com/mpcv3/045cac99-f948-478e-ae04-f8c161dcb9e2_1568132508.1920x1080at3000_h264.mp4" text="Regarder une vidéo de démonstration"

>[!IMPORTANT]
>
>Cette fonctionnalité est disponible uniquement pour les instances Campaign Classic.

## À propos des listes autorisées d’adresses IP {#about-ip-whitelisting}

Par défaut, votre instance Adobe Campaign Classic n’est pas accessible à partir de diverses adresses IP.

Si votre adresse IP n’a pas été ajoutée à la liste autorisée, vous ne pourrez pas vous connecter à l’instance à partir de cette adresse. De même, vous ne pourrez peut-être pas connecter une API à votre instance Message Center ou Marketing si l’adresse IP n’a pas été explicitement ajoutée à la liste autorisée avec l’instance.

Le panneau de contrôle vous permet de configurer de nouvelles connexions à vos instances en ajoutant des plages d’adresses IP à la liste autorisée. Pour ce faire, suivez la procédure ci-dessous.

Une fois les adresses IP ajoutées à la liste autorisée, vous pouvez créer des opérateurs Campaign et les associer à ces adresses afin que les utilisateurs puissent accéder à l’instance.

## Bonnes pratiques {#best-practices}

Veillez à suivre les recommandations et les limites ci-dessous lors de l’ajout des adresses IP à la liste autorisée dans le panneau de contrôle.

* **N’activez pas l’accès IP à tous les types d’accès** si vous ne souhaitez pas que l’adresse IP se connecte à vos serveurs RT ou votre zone de sécurité AEM.
* **Si vous avez provisoirement activé l’accès à votre instance pour une adresse IP**, assurez-vous de supprimer les adresses IP de la liste autorisée une fois que vous n’en avez plus besoin pour vous connecter à votre instance.
* **Nous vous déconseillons d’ajouter les adresses IP des lieux publics (aéroports, hôtels, etc.) à la liste autorisée**. Utilisez l’adresse VPN de votre entreprise pour assurer la sécurité permanente de votre instance.

## Ajouter des adresses IP à la liste autorisée pour l’accès aux instances {#whistelisting-ip-addresses}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange_add"
>title="Ajouter une plage d’adresses IP"
>abstract="Définissez la plage d’adresses IP que vous souhaitez ajouter à la liste autorisée pour vous connecter à votre instance."

Pour ajouter des adresses IP à la liste autorisée, procédez comme suit :

1. Ouvrez la carte **[!UICONTROL Paramètres des instances]** pour accéder à l’onglet des listes autorisées d’adresses IP, puis cliquez sur **[!UICONTROL Ajouter une plage d’adresses IP]**.

   >[!NOTE]
   >
   >Si la carte Paramètres des instances n’est pas visible sur la page d’accueil du panneau de contrôle, cela signifie que votre identifiant de l’organisation IMS n’est associé à aucune instance Adobe Campaign Classic.

   ![](assets/ip_whitelist_list1.png)

1. Indiquez les informations correspondant à la plage d’adresses IP que vous souhaitez ajouter à la liste autorisée comme décrit ci-dessous.

   ![](assets/ip_whitelist_add1.png)

   * **[!UICONTROL Instance(s)]** : les instances auxquelles les adresses IP seront en mesure de se connecter. Plusieurs instances peuvent être manipulées en même temps. Par exemple, des listes autorisées d’adresses IP peuvent être créées à la fois pour les instances de production et de test via la même étape.
   * **[!UICONTROL Plage d’adresses IP]** : la plage d’adresses IP à ajouter à la liste autorisée, au format CIDR. Veuillez noter qu’une plage d’adresses IP ne peut pas chevaucher une plage existante dans la liste autorisée. Dans ce cas, supprimez d’abord la plage qui contient l’adresse IP whitelistée.

   >[!NOTE]
   >
   >Le format CIDR (Classless Inter-Domain Routing) est le format pris en charge lors de l’ajout de plages d’adresses IP avec l’interface du panneau de contrôle. La syntaxe se compose d’une adresse IP, suivie d’un caractère « / » et d’un nombre décimal. Le format et sa syntaxe sont présentés en détail dans [cet article](https://whatismyipaddress.com/cidr).
   >
   >Vous pouvez rechercher sur Internet des outils en ligne gratuits qui vous permettront de convertir la plage IP qui vous intéresse au format CIDR.

   * **[!UICONTROL Libellé]** : libellé qui s’affichera dans la liste autorisée.
   * **[!UICONTROL Nom]** : le nom doit être unique pour le type d’accès, l’instance (dans le cas d’une connexion API externe) et l’adresse IP.


1. Spécifiez le type d’accès que vous souhaitez accorder aux adresses IP :

   * **[!UICONTROL Accès via la Console Campaign]** : les adresses IP seront autorisées à se connecter à la console Campaign Classic. Notez que l’accès à la console n’est activé que pour les instances Marketing. L’accès aux instances MID et RT n’est pas autorisé et n’est donc pas activé.
   * **[!UICONTROL Connexion via AEM]** : les adresses IP AEM spécifiées seront autorisées à se connecter à l’instance Marketing.
   * **[!UICONTROL Connexion via une API externe]** : les API externes ayant les adresses IP spécifiées seront autorisées à se connecter aux instances Marketing et/ou Message Center (RT). Notez que la connexion à la console des instances RT n’est pas activée.

   ![](assets/ip_whitelist_acesstype.png)

1. Cliquez sur le bouton **[!UICONTROL Enregistrer]**. La plage d’adresses IP est ajoutée à la liste autorisée.

   ![](assets/ip_whitelist_added.png)

Pour supprimer des plages d’adresses IP de la liste autorisée, sélectionnez-les puis cliquez sur le bouton **[!UICONTROL Supprimer une plage d’adresses IP]**.

**Rubriques connexes :**
* [Listes autorisées d’adresses IP (tutoriel vidéo)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/ip-allow-listing.html)
* [Liaison d’une zone de sécurité à un opérateur](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Linking_a_security_zone_to_an_operator)
