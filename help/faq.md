---
product: campaign
solution: Campaign
title: FAQ sur le Panneau de contrôle
description: Questions courantes relatives au Panneau de contrôle
feature: Control Panel
role: Architect
level: Intermediate
exl-id: 4f329764-ed8b-4939-affc-ed994fd6101d
source-git-commit: c834ae7226ed9dd1f78d4f4511b52cb5f04abfae
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 78%

---

# Forum aux questions {#faq}

## Panneau de contrôle {#control-panel}

### Qu’est-ce que le Panneau de contrôle ?

Dans le Panneau de contrôle, les administrateurs du produit peuvent gérer directement divers paramètres et contrôler la capacité des serveurs SFTP connectés à Adobe Campaign.

### Quelles sont les principales fonctionnalités du Panneau de contrôle ?

Le Panneau de contrôle vous permet de surveiller le stockage, d’ajouter des adresses IP à la liste autorisée et de gérer les clés SSH de vos serveurs SFTP en fonction de vos besoins et d’autres actions.

Pour plus d’informations, consultez la documentation relative aux actions prises en charge par le Panneau de contrôle.

### Existe-t-il des fonctionnalités non encore prises en charge sur Campaign v8 mais disponibles sur Campaign Classic v7 ?{#v8-restrictions}

Non. Toutes les fonctionnalités disponibles sur Campaign v7 sont désormais prises en charge par le Panneau de contrôle sur Campaign v8, notamment les fonctions liées à la gestion des sous-domaines et des certificats.

### Le Panneau de contrôle est-il réservé à Adobe Campaign ?

Oui, dans le Panneau de contrôle, vous pouvez gérer uniquement les paramètres d’Adobe Campaign.

### Puis-je utiliser le Panneau de contrôle ?

Le Panneau de contrôle n’est accessible que par les administrateurs de produit de nos clients actuels pour lesquels Adobe Campaign est hébergé sur AWS.

Le panneau de contrôle permet aux clients disposant d’un modèle d’hébergement hybride de tirer parti des fonctionnalités spécifiques du panneau de contrôle. Pour ce faire, ils doivent fournir l’URL de l’instance MID/RT configurée dans leur instance marketing dans le panneau de contrôle. [En savoir plus](instances-settings/using/external-accounts.md)

Si vous n’êtes pas administrateur, mais que vous souhaitez y accéder, veuillez contacter votre administrateur de produit pour qu’il vous ajoute en tant qu’administrateur.

### En tant qu’utilisateur de Campaign Classic v7, quelles sont les conditions d’accès au Panneau de contrôle ? {#v7-restrictions}

Le Panneau de contrôle est accessible aux utilisateurs administrateurs uniquement. [En savoir plus](discover/using/managing-permissions.md).

Pour Campaign v7, notez que votre instance doit être hébergée sur Amazon Web Services (AWS) et mise à niveau vers le dernier [build stable de Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=fr#rn-statuses) ou vers le build 9032 ou supérieur. Découvrez comment vérifier votre version de Campaign Classic v7 dans [cette section](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=fr#getting-your-campaign-version). Pour vérifier si votre instance Campaign Classic est hébergée sur AWS, suivez les étapes présentées dans [cette section](#hosted-aws).

### Comment puis-je accéder au Panneau de contrôle ?

Consultez les instructions détaillées dans la documentation relative à l’accès au Panneau de contrôle.

### Y a-t-il des frais supplémentaires pour l’utilisation du Panneau de contrôle ?

Non, il n’y a pas de frais supplémentaires si vous êtes déjà client Adobe Campaign.

## Identifiant de l’organisation {#ims-org-id}

### Qu’est-ce qu’un ID d’organisation ?

Il s’agit d’un identifiant unique attribué à votre instance lorsque vous vous connectez pour la première fois à Adobe Experience Cloud. Il doit être au format : xxx@AdobeOrg.

Pour plus d’informations, voir la [documentation relative à Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=fr).

### Où puis-je trouver mon ID d’organisation ?

Une méthode consiste à accéder à la [page d’accueil d’Adobe Experience Cloud](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]**. L’ID d’organisation se trouve au bas de l’onglet Administration. **[!UICONTROL Accès rapide]** . Vous trouverez des informations plus détaillées dans la [documentation Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).

Vous pouvez aussi lancer **Admin Console**. L’ID d’organisation est visible dans votre URL. Il doit se présenter comme suit : https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

### Pourquoi ai-je besoin de connaître mon ID d’organisation ?

Pour que vous puissiez gérer les paramètres de votre instance, nous voulons nous assurer que vous obtenez les informations adéquates pour la bonne instance au cas où vous utilisez plusieurs instances pour votre entreprise.

### Que faire si je dispose de plusieurs ID d’organisation ?

Si vous avez accès à plusieurs solutions Adobe, vous pouvez disposer de plusieurs ID d’organisation. Dans ce cas, l’ID d’organisation correct à utiliser est celui qui s’affiche sous votre instance Adobe Campaign.

>[!NOTE]
>
>Si vous disposez du même ID d’organisation pour Adobe Campaign et Adobe Analytics, c’est une excellente nouvelle. Disposer d’un identifiant d’organisation entre Analytics et Campaign est nécessaire si vous prévoyez d’intégrer les solutions afin de tirer parti des cas pratiques complexes tels que l’abandon du panier d’achat (pour AA + AC).
>
>Si vous disposez de ID d’organisation différents pour Adobe Campaign et Adobe Analytics, contactez l’assistance clientèle pour qu’ils soient harmonisés.

### Comment puis-je savoir si mon instance Adobe Campaign est hébergée sur AWS ?{#hosted-aws}

Pour vérifier si votre instance est hébergée sur AWS, procédez comme suit :

1. Récupérez votre URL de connexion. S’il s’agit de l’URL que vous utilisez pour vous connecter à votre instance Campaign, elle doit se terminer par « .campaign.adobe.com » ou « .neolane.net ».
1. Ouvrez le terminal, puis exécutez une opération **[!DNL nslookup]** sur votre URL de connexion.

   `doe-macOS% nslookup myinstance.campaign.adobe.com`

1. La réponse renvoie des informations sur votre instance.

   ```
   doe-macOS% nslookup myinstance.campaign.adobe.com
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   myinstance.campaign.adobe.com
   canonical name = myinstance-mkt-prod1.campaign.adobe.com.
   myinstance-mkt-prod1.campaign.adobe.com
   canonical name = myinstance-mkt-prod1-1.campaign.adobe.com.
   Name: myinstance-mkt-prod1-1.campaign.adobe.com
   Address: 12.34.567.89
   ```

1. Exécutez une opération **nslookup** sur l’adresse IP renvoyée.

   `doe-macOS% nslookup 12.34.567.89`

1. Vérifiez la valeur « name » dans le résultat renvoyé. Si elle contient « amazonaws.com », alors votre instance est hébergée sur AWS.

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>Si vous souhaitez que votre instance soit migrée vers AWS, contactez votre responsable client.
