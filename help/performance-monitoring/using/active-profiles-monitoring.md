---
title: Surveillance active des profils
description: Découvrez comment obtenir des informations en temps réel sur l’utilisation et l’évolution des Profils actifs les plus récents et historiques pour chacune de vos instances Campaign.
translation-type: tm+mt
source-git-commit: 024eb750021ff2446b34d648b5abfb016eabc289
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 17%

---


# Surveillance active des profils {#active-profiles-monitoring}

>[!IMPORTANT]
>
>La surveillance des profils actifs à partir du Panneau de configuration est disponible en version bêta et peut faire l&#39;objet de mises à jour fréquentes et de modifications sans préavis.
>
>Cette fonctionnalité est disponible pour les clients hébergés sur AWS depuis Campaign Standard 10368 build et Campaign Classic 8931 build. Si vous utilisez une version précédente, vous devez effectuer la mise à niveau pour utiliser cette fonctionnalité.

## A propos des profils actifs {#about-active-profiles}

Conformément à votre contrat, chacune de vos instances Campaign est configurée avec un nombre spécifique de profils actifs comptabilisés à des fins de facturation. Consultez votre dernier contrat pour connaître le nombre de profils actifs achetés.

Un “Profil” désigne un enregistrement d&#39;informations (par exemple : un enregistrement dans la table nmsRecipient ou une table externe contenant un identifiant de cookie, un identifiant client, un identifiant mobile ou d&#39;autres informations relatives à un canal particulier) représentant un client final ou un prospect.

Les Profils sont considérés comme actifs s&#39;ils ont été ciblés ou communiqués par un canal au cours des 12 derniers mois.

>[!NOTE]
>
>Les canaux Facebook et Twitter ne sont pas prises en compte.

Pour plus d&#39;informations sur les profils actifs, reportez-vous aux documentations [Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) et [Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) .

## Surveillance des profils actifs {#monitoring-active-profiles}

Le Panneau de configuration vous permet de surveiller l’utilisation des profils actifs pour chacune de vos instances Campaign.

Pour ce faire, procédez comme suit :

1. Open the **[!UICONTROL Performance Monitoring]** card, then select the **[!UICONTROL Active Profiles]** tab.

1. Sélectionnez l’instance de votre choix dans la **[!UICONTROL Liste d’instances]**.

1. Le nombre de profils actifs utilisés par l&#39;instance s&#39;affiche, ainsi que la dernière fois que le processus de facturation a été exécuté sur votre instance.

![](assets/active-profiles-graph.png)

>[!NOTE]
>
>Les profils actifs sont comptabilisés en fonction des workflows techniques dédiés qui s’exécutent tous les jours sur vos instances :
>
>* Processus [&quot;Facturation&quot;](https://docs.adobe.com/help/fr-FR/campaign-standard/using/administrating/application-settings/technical-workflows.html) pour Campaign Standard,
>* Processus [&quot;Nombre de profils de facturation actifs&quot;](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/technical-workflows/deliveries.html) pour Campaign Classic.


La zone inférieure fournit une représentation graphique de l&#39;utilisation des profils actifs au cours des 30 derniers jours. Vous pouvez remplacer la période affichée par 1 an en utilisant les filtres disponibles dans le coin supérieur droit.

Passez la souris sur l’une des barres de graphique pour obtenir le nombre exact de profils actifs utilisés sur la période sélectionnée.
