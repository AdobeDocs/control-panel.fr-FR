---
product: campaign
solution: Campaign
title: Surveillance des profils actifs
description: Découvrez comment obtenir des informations en temps réel sur l’utilisation et l’évolution des profils actifs les plus récents et historiques pour chacune de vos instances Campaign.
feature: Panneau de contrôle
role: Architect
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: c29b6d4bf59628a10f6b8e402176b1835770fc54
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 88%

---

# Surveillance des profils actifs {#active-profiles-monitoring}

## À propos des profils actifs {#about-active-profiles}

>[!IMPORTANT]
>
>La surveillance des profils actifs depuis le panneau de contrôle est disponible en version bêta et sujette à de fréquentes mises à jour et modifications sans préavis. Elle est disponible à partir de la version Campaign Standard 10368.

Conformément à votre contrat, chacune de vos instances Campaign est configurée avec un nombre spécifique de profils actifs comptabilisés à des fins de facturation. Consultez votre dernier contrat pour connaître le nombre de profils actifs achetés.

Un « Profil » désigne un enregistrement d’informations (par exemple : un enregistrement dans la table nmsRecipient ou une table externe contenant un identifiant de cookie, un identifiant client, un identifiant mobile ou d’autres informations relatives à un canal particulier) représentant un client final ou un prospect.

Les profils sont considérés comme actifs s’ils ont été ciblés ou ont fait l’objet d’une communication via un canal au cours des 12 derniers mois.

>[!NOTE]
>
>Les canaux Facebook et Twitter ne sont pas pris en compte.

Pour plus d’informations sur les profils Principaux, reportez-vous aux documentations [Campaign Standard](https://https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) et [Campaign Classic v7](https://https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles).

## Surveillance des profils actifs {#monitoring-active-profiles}

Le panneau de contrôle permet de surveiller l’utilisation des profils actifs pour chacune de vos instances Campaign.

Pour ce faire, procédez comme suit :

1. Ouvrez la carte **[!UICONTROL Suivi des performances]**, puis sélectionnez l’onglet **[!UICONTROL Profils actifs]**.

1. Sélectionnez l’instance de votre choix dans la **[!UICONTROL Liste d’instances]**.

1. Le nombre de profils actifs utilisés par l’instance s’affiche, ainsi que la dernière fois que le workflow de facturation a été exécuté sur votre instance.

![](assets/active-profiles-graph.png)

>[!NOTE]
>
>Les profils actifs sont comptabilisés en fonction des workflows techniques dédiés qui s’exécutent tous les jours sur vos instances :
>
>* workflow [« Facturation »](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=en) pour Campaign Standard ;
>* workflow [« Nombre de profils de facturation actifs »](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html?lang=fr#automating-with-workflows) pour Campaign Classic.


La zone inférieure contient une représentation graphique de l’utilisation des profils actifs au cours des 30 derniers jours. Vous pouvez modifier la période affichée sur 1 an à l’aide des filtres proposés dans l’angle supérieur droit.

Pointez sur l’une des barres de graphique pour obtenir le nombre exact de profils actifs utilisés au cours de la période sélectionnée.
