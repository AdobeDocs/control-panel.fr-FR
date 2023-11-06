---
product: campaign
solution: Campaign
title: Détails de l’instance
description: Découvrez comment surveiller les détails de votre instance dans le Panneau de contrôle
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 02819bfc-9886-43fc-8014-9bfe64c42048
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '536'
ht-degree: 100%

---

# Détails de lʼinstance {#instance-details}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_instancedetails"
>title="À propos des détails de lʼinstance"
>abstract="Affichez les détails de vos instances Adobe Campaign : types, noms, informations de build et recommandations de mises à niveau éventuelles."

## À propos des détails de l’instance {#about-instance-details}

>[!IMPORTANT]
>
>Cette fonctionnalité est disponible uniquement pour les instances Campaign v7/v8.

L’architecture de votre instance Adobe Campaign peut contenir plusieurs serveurs pour garantir la flexibilité des activités marketing. Par exemple, des serveurs Marketing, Real Time (ou Message Center) et Mid-sourcing peuvent prendre en charge votre instance.

La fonctionnalité Détails de l’instance vous permet d’afficher l’architecture plane de votre instance. En plus de fournir des informations sur le serveur, elle vous permet également de savoir si le build de votre instance est à jour ou pas et vous indique les upgrades recommandés lorsque cela est nécessaire.

>[!NOTE]
>
>Nous vous recommandons de mettre vos instances à niveau au moins une fois par an afin dʼéviter une dégradation des performances et de pouvoir profiter des fonctionnalités et des correctifs les plus récents quʼAdobe Campaign v7/v8 offre.

**Rubriques connexes :**

* [Réalisation d’un upgrade de build](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/updating-adobe-campaign/build-upgrade.html?lang=fr)
* [Mise à jour d’Adobe Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/updating-adobe-campaign/introduction.html?lang=fr)

## Récupération d’informations sur vos instances {#retrieving-information-about-instances}

Pour obtenir des informations sur les serveurs connectés à vos instances, procédez comme suit :

1. Ouvrez la carte **[!UICONTROL Paramètres des instances]** pour accéder à l’onglet **[!UICONTROL Détails de l’instance]**.

   >[!NOTE]
   >
   >Si la vignette Paramètres des instance nʼest pas visible sur la page dʼaccueil du Panneau de contrôle, cela signifie que votre identifiant dʼorganisation nʼest associé à aucune instance Adobe Campaign v7/v8.

1. Dans le panneau de gauche, sélectionnez l’instance Campaign désirée.

   >[!NOTE]
   >
   >Toutes vos instances Campaign sʼaffichent dans la liste du volet gauche. La fonctionnalité Détails de l’instance étant réservée aux instances Campaign v7/v8, le message « Instance non applicable » s’affiche si vous sélectionnez une instance Campaign Standard.

1. Les serveurs connectés à l’instance s’affichent.

   ![](assets/instance_details.png)

Les informations disponibles sont les suivantes :

* **[!UICONTROL Type]** : type du serveur. Les valeurs possibles sont MKT (Marketing), MID (Mid-sourcing) et RT (Message Center/Real-time messaging).
* **[!UICONTROL Nom]** : nom du serveur.
* **[!UICONTROL Build]** : la version de build installée sur le serveur.
* **[!UICONTROL Infos sur la mise à niveau]** : cette colonne vous indique si une mise à jour est requise pour le serveur.
   * Vert : votre serveur est à jour et aucun upgrade n’est requis.
   * Jaune : vous devez envisager un upgrade. Vous ne disposez pas des fonctionnalités et des correctifs les plus récents.
   * Rouge : effectuez un upgrade dès que possible. Vous ne disposez pas des nouvelles fonctionnalités et les performances du serveur ne sont peut-être pas optimales.

Si l’un de vos serveurs nécessite un upgrade, reportez-vous à [cette documentation](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/updating-adobe-campaign/build-upgrade.html?lang=fr) pour plus de détails sur la manière de procéder.

## Questions courantes {#common-questions}

**Je ne vois pas le serveur MID dans l’architecture de mon instance ; cela veut-il dire que mes instances ne fonctionnent pas correctement ? Ai-je besoin de l’instance RT pour une tâche que je ne suis pas en mesure d’effectuer aujourd’hui ?**

Votre propre instance peut sembler très différente et ne pas disposer de tous les types de serveurs, ou peut disposer de plusieurs instances du même serveur. Ne pas disposer d’un type de serveur ou d’un autre ne signifie pas que vous ne pouvez pas envoyer un message en temps réel ou effectuer d’autres types d’activités. Vous pouvez demander de la capacité de serveur supplémentaire. Dans ce cas, des frais supplémentaires s’appliqueront.

Contactez l’assistance clientèle si vous pensez que certains serveurs n’apparaissent pas sur la page Détails de l’instance. Veillez à indiquer l’URL de l’instance spécifique dans votre message.
