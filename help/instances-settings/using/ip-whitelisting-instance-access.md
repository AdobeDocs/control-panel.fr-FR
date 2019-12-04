---
title: Liste blanche IP
description: En savoir plus sur la liste blanche des adresses IP dans le Panneau de configuration, par exemple l’accès
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# IP whitelisting {#ip-whitelisting}

>[!CAUTION]
>
>Cette fonctionnalité est disponible uniquement pour les instances Campaign Classic.

## A propos de la mise en whiteliste d'adresses IP {#about-ip-whitelisting}

Par défaut, votre instance Adobe Campaign Classic n’est pas accessible à partir de plusieurs adresses IP.

Si votre adresse IP n'a pas été whitelistée, vous ne pourrez pas vous connecter à l'instance à partir de cette adresse. De la même manière, il se peut que vous ne puissiez pas connecter une API à votre Centre de messages ou instance Marketing si l’adresse IP n’a pas été explicitement mise en liste blanche avec l’instance.

Le panneau de contrôle vous permet de configurer de nouvelles connexions à vos instances en whitelistant des plages d'adresses IP. Pour ce faire, suivez la procédure ci-dessous.

Une fois les adresses IP whitelistées, vous pouvez créer des opérateurs Campaign et les lier à ces adresses afin que les utilisateurs puissent accéder à l'instance.

## Bonnes pratiques {#best-practices}

Veillez à suivre les recommandations et les limites ci-dessous lors de la mise en whiteliste des adresses IP dans le panneau de contrôle.

* **N'activez pas l'accès IP à tous les types d'accès** si vous ne souhaitez pas que l'adresse IP se connecte à vos serveurs RT ou votre zone de sécurité AEM.
* **Si vous avez temporairement activé l’accès à votre instance pour une adresse** IP, veillez à supprimer les adresses IP des adresses IP placées sur liste blanche une fois que vous n’avez plus besoin de vous connecter à votre instance.
* **Nous vous déconseillons de faire une liste blanche des adresses IP des lieux** publics (aéroports, hôtels, etc.). Utilisez le VPN de votre entreprise pour assurer la sécurité permanente de votre instance.

## Mise en whiteliste d'adresses IP pour l'accès aux instances {#whistelisting-ip-addresses}

Pour mettre en liste blanche les adresses IP, procédez comme suit :

1. Ouvrez la **[!UICONTROL carte Paramètres des instances]** pour accéder à l’onglet Liste blanche des adresses IP, puis cliquez sur **[!UICONTROL Ajouter une nouvelle plage d’adresse IP]**.

   >[!NOTE]
   >
   >Si la vignette Paramètres des instances n'est pas visible sur la page d'accueil du panneau de contrôle, cela signifie que votre identifiant de l'organisation IMS n'est associé à aucune instance Adobe Campaign Classic.

   ![](assets/ip_whitelist_list1.png)

1. Indiquez les informations correspondant à la plage IP que vous souhaitez whitelister comme décrit ci-dessous.

   ![](assets/ip_whitelist_add1.png)

   * **[!UICONTROL Instance(s)]**: instances auxquelles les adresses IP pourront se connecter. Plusieurs instances peuvent être manipulées en même temps. Par exemple, des adresses IP peuvent être whitelistées à la fois pour les instances de production et de test via la même étape.
   * **[!UICONTROL Plage]** IP : Plage d’adresses IP à mettre en liste blanche, au format CIDR. Notez qu'une plage IP ne peut pas contenir une plage whitelistée existante. Dans ce cas, supprimez d'abord la plage qui contient l'IP whitelistée.
   >[!NOTE]
   >
   >Le format CIDR (Classless Inter-Domain Routing) est le format pris en charge lors de l'ajout de plages IP avec l'interface du panneau de contrôle. La syntaxe se compose d'une adresse IP, suivie d'un caractère / et d'un nombre décimal. Le format et sa syntaxe sont présentés en détail dans [cet article](https://whatismyipaddress.com/cidr).
   >
   >Vous pouvez rechercher sur Internet des outils en ligne gratuits qui vous permettront de convertir la plage IP qui vous intéresse au format CIDR.

   * **!UICONTROL Libellé]**: Libellé qui s’affichera dans la liste des adresses IP en liste blanche.
   * **[!UICONTROL Nom]**: Le nom doit être unique pour le type d’accès, l’instance (en cas de connexion à l’API externe) ainsi que l’adresse IP.


1. Spécifiez le type d’accès que vous souhaitez accorder aux adresses IP :

   * **[!UICONTROL Accès]**&#x200B;à la console de campagne : Les adresses IP seront autorisées à se connecter à la console Campaign Classic. Notez que l'accès à la console n'est activé que pour les instances Marketing. L'accès aux instances MID et RT n'est pas autorisé et n'est donc pas activé.
   * **[!UICONTROL Connexion]** AEM : Les adresses IP AEM spécifiées seront autorisées à se connecter à l’instance Marketing.
   * **[!UICONTROL Connexion]**&#x200B;à l'API externe : Les API externes avec les adresses IP spécifiées seront autorisées à se connecter à l’instance Marketing et/ou Message Center (RT). Notez que la connexion à la console des instances RT n'est pas activée.
   ![](assets/ip_whitelist_acesstype.png)

1. Cliquez sur le bouton **[!UICONTROL Enregistrer.]** La plage IP est ajoutée à la liste des adresses IP whitelistées.

   ![](assets/ip_whitelist_added.png)

To delete whitelisted IP ranges, select them then click the **[!UICONTROL Delete IP range]** button.

**Rubriques connexes :**
* [Mise en whiteliste d'adresses IP (tutoriel vidéo)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/ip-whitelisting.html)
* [Liaison d'une zone de sécurité à un opérateur](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Linking_a_security_zone_to_an_operator)
