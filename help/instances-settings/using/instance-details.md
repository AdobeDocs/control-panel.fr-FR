---
title: Détails de l’instance
description: Découvrez comment surveiller les détails de votre instance dans le panneau de contrôle
translation-type: ht
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5

---


# Détails de l’instance {#instance-details}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_instancedetails"
>title="[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_instancedetails&quot;
>title=&quot;À propos des détails de l’instance&quot;
>abstract=&quot;Affichez les détails de vos instances Adobe Campaign : types, noms, informations de build et recommandations de mises à niveau possibles.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/fr-FR/campaign-classic/using/release-notes/latest-release.html&quot; text=&quot;Notes de mise à jour de Campaign Classic&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/fr-FR/campaign-standard/using/release-notes/release-notes.html&quot; text=&quot;Notes de mise à jour de Campaign Standard&quot;"
>abstract="[!IMPORTANT]"
>additional-url="Cette fonctionnalité est disponible uniquement pour les instances Campaign Classic." text="À propos des détails de l’instance {#about-instance-details}"
>additional-url="L’architecture de votre instance Adobe Campaign Classic peut contenir plusieurs serveurs pour garantir la flexibilité des activités marketing. Par exemple, des serveurs Marketing, Real Time (ou Message Center) et Mid-sourcing peuvent prendre en charge votre instance." text="La fonctionnalité Détails de l’instance vous permet d’afficher l’architecture plane de votre instance. En plus de fournir des informations sur le serveur, elle vous permet également de savoir si le build de votre instance est à jour ou pas et vous indique les upgrades recommandés lorsque cela est nécessaire."

>[!NOTE]
>
>Nous vous recommandons d’effectuer un upgrade de vos instances au moins une fois par an afin d’éviter une dégradation des performances et de pouvoir bénéficier des fonctionnalités et des correctifs les plus récents proposés par Adobe Campaign Classic.

## **Rubriques connexes :**

[Réalisation d’un upgrade de build[#$tu14]



>
>
>



* 
* 

## Dans le panneau de gauche, sélectionnez l’instance Campaign Classic désirée.{#retrieving-information-about-instances}

[!NOTE]

1. Toutes vos instances Campaign s&#39;affichent dans la liste du volet gauche. La fonctionnalité Détails de l’instance étant réservée aux instances Campaign Classic, le message « Instance non applicable » s’affiche si vous sélectionnez une instance Campaign Standard.********

   >[!NOTE]Les serveurs connectés à l’instance s’affichent.
   >
   >![](assets/instance_details.png)

1. Les informations disponibles sont les suivantes :

   >**[!UICONTROL Type]** : type du serveur. Les valeurs possibles sont MKT (Marketing), MID (Mid-sourcing) et RT (Message Center/Real-time messaging).
   >
   >**[!UICONTROL Nom]** : nom du serveur.

1. **[!UICONTROL Build]** : la version de build installée sur le serveur.

   **[!UICONTROL Infos sur la mise à niveau]** : cette colonne vous indique si une mise à jour est requise pour le serveur.

Vert : votre serveur est à jour et aucun upgrade n’est requis.

* **[!UICONTROL Jaune : vous devez envisager un upgrade. Vous ne disposez pas des fonctionnalités et des correctifs les plus récents.]**
* **[!UICONTROL Rouge : effectuez un upgrade dès que possible. Vous ne disposez pas des nouvelles fonctionnalités et les performances du serveur ne sont peut-être pas optimales.]**
* Si l’un de vos serveurs nécessite un upgrade, reportez-vous à [cette documentation[#$tu36] pour plus de détails sur la manière de procéder.]**
* 
   * 
   * 
   * 

If one of your servers requires to be upgraded, refer to [this documentation-ERR:REF-NOT-FOUND- for more details on how to proceed.

## Common questions {#common-questions}

**I do not see the MID server on my instance architecture, does it mean my instances are not functioning correctly? Do I need the RT instance for something I am not able to do today?**

Your own instance can look very different, and it may not have all types of servers, or it can have several of the same server. Not having one type of the server or another does not mean you cannot send a real-time message or perform other kinds of activities. You can request additional server capacity, additional fees will apply.

Please contact Customer Care if you believe some servers are not showing in the &quot;Instance Details&quot; page. Make sure you note the specific instance URL in your message.
