---
title: Détails de l’instance
description: Découvrez comment surveiller les détails de votre instance dans le panneau de contrôle
translation-type: tm+mt
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5

---


# Détails de l’instance {#instance-details}

>[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_instancedetails&quot;
>title=&quot;À propos des détails de l’instance&quot;
>abstract=&quot;Affichez les détails de vos instances Adobe Campaign : types, noms, informations de build et recommandations de mises à niveau possibles.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/fr-FR/campaign-classic/using/release-notes/latest-release.html&quot; text=&quot;Notes de mise à jour de Campaign Classic&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/fr-FR/campaign-standard/using/release-notes/release-notes.html&quot; text=&quot;Notes de mise à jour de Campaign Standard »

>[!IMPORTANT]
>
>Cette fonctionnalité est disponible uniquement pour les instances Campaign Classic.

## À propos des détails de l’instance {#about-instance-details}

L’architecture de votre instance Adobe Campaign Classic peut contenir plusieurs serveurs pour garantir la flexibilité des activités marketing. Par exemple, des serveurs Marketing, Real Time (ou Message Center) et Mid-sourcing peuvent prendre en charge votre instance.

La fonctionnalité Détails de l’instance vous permet d’afficher l’architecture plane de votre instance. En plus de fournir des informations sur le serveur, elle vous permet également de savoir si le build de votre instance est à jour ou pas et vous indique les upgrades recommandés lorsque cela est nécessaire.

>[!NOTE]
>
>Nous vous recommandons d’effectuer un upgrade de vos instances au moins une fois par an afin d’éviter une dégradation des performances et de pouvoir bénéficier des fonctionnalités et des correctifs les plus récents proposés par Adobe Campaign Classic.

**Rubriques connexes :**

* [Réalisation d’un upgrade de build](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html)
* [Mise à jour d’Adobe Campaign](https://docs.campaign.adobe.com/doc/AC/en/PRO_Updating_Adobe_Campaign_Introduction.html)

## Récupération d’informations sur vos instances {#retrieving-information-about-instances}

Pour obtenir des informations sur les serveurs connectés à vos instances, procédez comme suit :

1. Ouvrez la **[!UICONTROL Instances Settings]** carte pour accéder à l’ **[!UICONTROL Instance Details]** onglet.

   >[!NOTE]
   >
   >Si la carte Paramètres des instances n’est pas visible sur la page d’accueil du panneau de contrôle, cela signifie que votre identifiant de l’organisation IMS n’est associé à aucune instance Adobe Campaign Classic.

1. Dans le panneau de gauche, sélectionnez l’instance Campaign Classic désirée.

   >[!NOTE]
   >
   >Toutes vos instances Campaign s&#39;affichent dans la liste du volet gauche. La fonctionnalité Détails de l’instance étant réservée aux instances Campaign Classic, le message « Instance non applicable » s’affiche si vous sélectionnez une instance Campaign Standard.

1. Les serveurs connectés à l’instance s’affichent.

   ![](assets/instance_details.png)

Les informations disponibles sont les suivantes :

* **[!UICONTROL Type]** : type du serveur. Les valeurs possibles sont MKT (Marketing), MID (Mid-sourcing) et RT (Message Center/Real-time messaging).
* **[!UICONTROL Name]**: nom du serveur.
* **[!UICONTROL Build:]** version de build installée sur le serveur.
* **[!UICONTROL Upgrade info]**: cette colonne vous informe si une mise à jour est requise pour le serveur.
   * Vert : votre serveur est à jour et aucun upgrade n’est requis.
   * Jaune : vous devez envisager un upgrade. Vous ne disposez pas des fonctionnalités et des correctifs les plus récents.
   * Rouge : effectuez un upgrade dès que possible. Vous ne disposez pas des nouvelles fonctionnalités et les performances du serveur ne sont peut-être pas optimales.

Si l’un de vos serveurs nécessite un upgrade, reportez-vous à [cette documentation](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html) pour plus de détails sur la manière de procéder.

## Questions courantes {#common-questions}

**Je ne vois pas le serveur MID dans l’architecture de mon instance ; cela veut-il dire que mes instances ne fonctionnent pas correctement ? Ai-je besoin de l’instance RT pour une tâche que je ne suis pas en mesure d’effectuer aujourd’hui ?**

Votre propre instance peut sembler très différente et ne pas disposer de tous les types de serveurs, ou peut disposer de plusieurs instances du même serveur. Ne pas disposer d’un type de serveur ou d’un autre ne signifie pas que vous ne pouvez pas envoyer un message en temps réel ou effectuer d’autres types d’activités. Vous pouvez demander de la capacité de serveur supplémentaire ; des frais supplémentaires s’appliqueront.

Contactez l’Assistance clientèle si vous pensez que certains serveurs n’apparaissent pas sur la page « Détails de l’instance ». Veillez à indiquer l’URL de l’instance spécifique dans votre message.
