---
title: Mise en whiteliste d’adresses IP
description: Découvrez la mise en whiteliste d’adresses IP dans le panneau de contrôle pour l’accès aux instances
translation-type: tm+mt
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5

---


# Mise en whiteliste d’adresses IP {#ip-whitelisting}

>[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_iprange&quot;
>title=&quot;À propos de la mise en whiteliste d’adresses IP&quot;
>abstract=&quot;Gérez la mise en whiteliste d’adresses IP pour accéder à vos instances.&quot;
>additional-url=&quot;https://images-tv.adobe.com/mpcv3/045cac99-f948-478e-ae04-f8c161dcb9e2_1568132508.1920x1080at3000_h264.mp4&quot; text=&quot;Regarder la vidéo de démonstration&quot;

>[!IMPORTANT]
>
>Cette fonctionnalité est disponible uniquement pour les instances Campaign Classic.

## À propos de la mise en whiteliste d’adresses IP {#about-ip-whitelisting}

Par défaut, votre instance Adobe Campaign Classic n’est pas accessible à partir de diverses adresses IP.

Si votre adresse IP n’a pas été whitelistée, vous ne pourrez pas vous connecter à l’instance à partir de cette adresse. De même, vous ne pourrez peut-être pas connecter une API à votre instance Message Center ou Marketing si l’adresse IP n’a pas été explicitement whitelistée avec l’instance.

Le panneau de contrôle vous permet de configurer de nouvelles connexions à vos instances en whitelistant des plages d’adresses IP. Pour ce faire, suivez la procédure ci-dessous.

Une fois les adresses IP whitelistées, vous pouvez créer des opérateurs Campaign et les associer à ces adresses afin que les utilisateurs puissent accéder à l’instance.

## Bonnes pratiques {#best-practices}

Veillez à suivre les recommandations et les limites ci-dessous lors de la mise en whiteliste des adresses IP dans le panneau de contrôle.

* **N’activez pas l’accès IP à tous les types d’accès** si vous ne souhaitez pas que l’adresse IP se connecte à vos serveurs RT ou votre zone de sécurité AEM.
* **Si vous avez provisoirement activé l’accès à votre instance pour une adresse IP**, assurez-vous de supprimer les adresses IP de la whiteliste une fois que vous n’en avez plus besoin pour vous connecter à votre instance.
* **Il n’est pas recommandé de whitelister les adresses IP de lieux publics** (aéroports, hôtels, etc.). Utilisez l’adresse VPN de votre entreprise pour assurer la sécurité permanente de votre instance.

## Mise en whiteliste d’adresses IP pour l’accès aux instances {#whistelisting-ip-addresses}

>[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_iprange_add&quot;
>title=&quot;Ajouter une plage d’adresses IP&quot;
>abstract=&quot;Définissez la plage d’adresses IP que vous souhaitez whitelister pour vous connecter à votre instance.&quot;

Pour whitelister des adresses IP, procédez comme suit :

1. Ouvrez le **[!UICONTROL Instances Settings card]** pour accéder à l’onglet Liste blanche d’adresses IP, puis cliquez sur **[!UICONTROL Add new IP Range]**.

   >[!NOTE]
   >
   >Si la carte Paramètres des instances n’est pas visible sur la page d’accueil du panneau de contrôle, cela signifie que votre identifiant de l’organisation IMS n’est associé à aucune instance Adobe Campaign Classic.

   ![](assets/ip_whitelist_list1.png)

1. Indiquez les informations correspondant à la plage d’adresses IP que vous souhaitez whitelister comme décrit ci-dessous.

   ![](assets/ip_whitelist_add1.png)

   * **[!UICONTROL Instance(s)]**: instances auxquelles les adresses IP pourront se connecter. Plusieurs instances peuvent être manipulées en même temps. Par exemple, des adresses IP peuvent être whitelistées à la fois pour les instances de production et de test via la même étape.
   * **[!UICONTROL IP Range]**: Plage d’adresses IP à mettre en liste blanche, au format CIDR. Notez qu’une plage d’adresses IP ne peut pas contenir une plage whitelistée existante. Dans ce cas, supprimez d’abord la plage qui contient l’adresse IP whitelistée.
   >[!NOTE]
   >
   >Le format CIDR (Classless Inter-Domain Routing) est le format pris en charge lors de l’ajout de plages d’adresses IP avec l’interface du panneau de contrôle. La syntaxe se compose d’une adresse IP, suivie d’un caractère « / » et d’un nombre décimal. Le format et sa syntaxe sont présentés en détail dans [cet article](https://whatismyipaddress.com/cidr).
   >
   >Vous pouvez rechercher sur Internet des outils en ligne gratuits qui vous permettront de convertir la plage IP qui vous intéresse au format CIDR.

   * **[!UICONTROL Label]**: Libellé qui s’affichera dans le des adresses IP en liste blanche.
   * **[!UICONTROL Name]**: Le nom doit être unique pour le type d’accès, l’instance (en cas de connexion à l’API externe) ainsi que l’adresse IP.


1. Spécifiez le type d’accès que vous souhaitez accorder aux adresses IP :

   * **[!UICONTROL Campaign Console Access]**: Les adresses IP seront autorisées à se connecter à la console Campaign Classic. Notez que l’accès à la console n’est activé que pour les instances Marketing. L’accès aux instances MID et RT n’est pas autorisé et n’est donc pas activé.
   * **[!UICONTROL AEM connection]**: Les adresses IP AEM spécifiées seront autorisées à se connecter à l’instance Marketing.
   * **[!UICONTROL External API connection]**: Les API externes avec les adresses IP spécifiées seront autorisées à se connecter à l’instance Marketing et/ou Message Center (RT). Notez que la connexion à la console des instances RT n’est pas activée.
   ![](assets/ip_whitelist_acesstype.png)

1. Cliquez sur le **[!UICONTROL Save]** bouton. La plage d’adresses IP est ajoutée à la liste des adresses IP whitelistées.

   ![](assets/ip_whitelist_added.png)

To delete whitelisted IP ranges, select them then click the **[!UICONTROL Delete IP range]** button.

**Rubriques connexes :**
* [Mise en whiteliste d’adresses IP (tutoriel vidéo)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/ip-whitelisting.html)
* [Liaison d’une zone de sécurité à un opérateur](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Linking_a_security_zone_to_an_operator)
