---
product: campaign
solution: Campaign
title: À propos de la surveillance des bases de données
description: Découvrez comment surveiller les performances de votre base de données Campaign dans le panneau de contrôle
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: 76301a1e222da17a2b4fd58d68d24efd04b07b1c
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 100%

---

# À propos de la surveillance des bases de données {#database-monitoring}

## À propos des bases de données d’instances {#about-instances-databases}

Conformément à votre contrat, chacune de vos instances Campaign est dotée d’un espace de base de données spécifique.

Les bases de données englobent les **ressources**, les **workflows** et les **données** stockées dans Adobe Campaign.

Au fil du temps, elles peuvent atteindre leur capacité maximale, en particulier si les ressources stockées ne sont jamais supprimées de l’instance ou si de nombreux workflows sont mis en pause.

Le dépassement de la capacité d’une base de données d’instance peut entraîner différents problèmes (impossibilité de se connecter, d’envoyer des emails, etc.). La surveillance des bases de données d’instances est donc essentielle pour garantir des performances optimales.

## Surveillance de l’utilisation des bases de données{#monitoring-database-usage}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_database"
>title="À propos de la surveillance des bases de données"
>abstract="Dans cet onglet, vous obtenez des informations en temps réel sur l’utilisation et l’évolution les plus récentes et historiques des bases de données pour chacune de vos instances Campaign."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=fr" text="À propos du suivi des performances"

Le Panneau de contrôle permet de surveiller l’utilisation de la base de données pour chacune de vos instances Campaign. Pour ce faire, ouvrez la carte **[!UICONTROL Suivi des performances]**, puis sélectionnez l’onglet **[!UICONTROL Bases de données]**.

Sélectionnez l’instance de votre choix dans la **[!UICONTROL Liste d’instances]** pour afficher des informations sur la capacité de la base de données et l’espace utilisé pour cette instance.

En outre, vous pouvez recevoir des notifications lorsque l’une de vos bases de données atteint sa limite de capacité. Pour cela, abonnez-vous aux [alertes par email](../../performance-monitoring/using/email-alerting.md).

>[!NOTE]
>
>Si la quantité d’espace de base de données disponible, indiquée dans le panneau de contrôle, ne correspond pas à la quantité spécifiée dans votre contrat, contactez l’assistance clientèle.

![](assets/databases_dashboard.png)

Les données de ce tableau de bord sont mises à jour en fonction du **[!UICONTROL workflow technique de nettoyage de la base de données]** qui s’exécute sur votre instance Campaign (voir la documentation de [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=fr#list-of-technical-workflows) et de [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html?lang=fr)). Vous pouvez vérifier la dernière fois que le workflow s’est exécuté au-dessous des mesures **[!UICONTROL Espace utilisé]** et **[!UICONTROL Espace fourni]**. Si le workflow n’est pas en cours d’exécution depuis plus de 3 jours, nous recommandons de contacter l’assistance clientèle d’Adobe pour examiner les raisons pour lesquelles il ne fonctionne pas.

D’autres mesures sont disponibles dans ce tableau de bord pour vous aider à analyser l’utilisation de la base de données de l’instance. Elles sont détaillées dans les sections suivantes :

* [Utilisation de la base de données](../../performance-monitoring/using/database-utilization.md)
* [Présentation de l’espace de stockage](../../performance-monitoring/using/database-storage-overview.md)
* [Top 10 des ressources temporaires](../../performance-monitoring/using/database-top-ten-resources.md)
* [Requêtes actives](../../performance-monitoring/using/database-active-queries.md)

![](assets/do-not-localize/how-to-video.png) Découvrez cette fonctionnalité en vidéo dans [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=fr#performance-monitoring) ou [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=fr#performance-monitoring).
