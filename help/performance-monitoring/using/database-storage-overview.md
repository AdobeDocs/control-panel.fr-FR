---
product: campaign
solution: Campaign
title: Vue d’ensemble de l’espace de stockage
description: Découvrez comment surveiller, dans le panneau de contrôle, les différentes ressources Campaign qui occupent de l’espace de base de données sur vos instances.
feature: Control Panel
role: Admin
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: e8bffd8e7f571fd85c725adf837c2997f7615fcd
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 100%

---

# Vue d’ensemble de l’espace de stockage {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="À propos de la vue d’ensemble de l’espace de stockage"
>abstract="Dans cet onglet, vous trouverez des informations détaillées sur les différentes ressources de Campaign qui consomment de l’espace sur la base de données."

La zone **[!UICONTROL Présentation de l’espace de stockage]** contient une représentation graphique de l’espace occupé par :

* **[!UICONTROL Ressources du système]**

  Notez que si les ressources du système consomment une grande partie de l’espace de la base de données, nous recommandons de contacter l’assistance clientèle.

* **[!UICONTROL Tables d’usine]** fournies par défaut avec vos instances Campaign
* **[!UICONTROL Tables temporaires]** créées par les workflows et les diffusions
* **[!UICONTROL Tables à configurer]** générées après la création de ressources personnalisées

![](assets/database-storage-overview.png)

Cliquez sur le bouton **[!UICONTROL Afficher les détails]** pour obtenir davantage de détails sur les différentes ressources qui consomment de l’espace de base de données.

Vous pouvez utiliser la liste déroulante pour affiner votre recherche et afficher les tableaux d’un type de ressource spécifique uniquement (workflows, diffusions, destinataires).

![](assets/database-storage-details.png)

Notez que cet écran vous permet également de surveiller les paramètres de workflow qui peuvent nécessiter une attention particulière pour éviter tout problème sur vos instances. En savoir plus sur [cette page](workflow-monitoring.md).
