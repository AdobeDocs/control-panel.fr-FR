---
product: campaign
solution: Campaign
title: FAQ sur le panneau de contrôle
description: Questions courantes relatives au panneau de contrôle
feature: Control Panel
role: Architect
level: Intermediate
exl-id: 4f329764-ed8b-4939-affc-ed994fd6101d
source-git-commit: cca04cd965c00a9e2bc496de632ee41ce53a166a
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 97%

---

# Forum aux questions {#faq}

## Panneau de contrôle {#control-panel}

### Qu’est-ce que le panneau de contrôle ?

Dans le panneau de contrôle, les administrateurs du produit peuvent gérer directement divers paramètres et contrôler la capacité des serveurs SFTP connectés à Adobe Campaign.

### Quelles sont les principales fonctionnalités du panneau de contrôle ?

Le panneau de contrôle vous permet de surveiller le stockage, d’ajouter des adresses IP à la liste autorisée et de gérer les clés SSH de vos serveurs SFTP en fonction de vos besoins et d’autres actions.

Pour plus d’informations, consultez la documentation relative aux actions prises en charge par le panneau de contrôle.

### Quelles sont les fonctionnalités non prises en charge dans Campaign v8 mais disponibles dans Campaign Classic v7 ?{#v8-restrictions}

Les fonctions liées à la gestion des sous-domaines et des certificats ne sont pas encore prises en charge par le panneau de contrôle sur Campaign v8. Contactez l’assistance clientèle de Campaign pour toute assistance s’y rapportant.

### Le panneau de contrôle est-il réservé à Adobe Campaign ?

Oui, dans le panneau de contrôle, vous pouvez gérer uniquement les paramètres d’Adobe Campaign.

### Puis-je utiliser le panneau de contrôle ?

Le panneau de contrôle n’est accessible que par les administrateurs de produit de nos clients actuels pour lesquels Adobe Campaign est hébergé sur AWS. Notez que les environnements hybrides ne sont pas encore pris en charge.

Si vous n’êtes pas administrateur, mais que vous souhaitez y accéder, veuillez contacter votre administrateur de produit pour qu’il vous ajoute en tant qu’administrateur.

### En tant qu’utilisateur de Campaign Classic v7, quelles sont les conditions d’accès au panneau de contrôle ? {#v7-restrictions}

Le panneau de contrôle est accessible aux utilisateurs administrateurs uniquement. [En savoir plus](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html#discover-control-panel).

Pour Campaign Classic v7, veuillez noter que votre instance doit être hébergée sur Amazon Web Services (AWS) et mise à niveau vers le dernier build [Campaign GA](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=fr#rn-statuses). Découvrez comment vérifier votre version de Campaign Classic dans [cette section](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=fr#getting-your-campaign-version). Pour vérifier si votre instance Campaign Classic est hébergée sur AWS, suivez les étapes présentées dans [cette section](#hosted-aws).

### Comment puis-je accéder au panneau de contrôle ?

Consultez les instructions détaillées dans la documentation relative à l’accès au panneau de contrôle.

### Y a-t-il des frais supplémentaires pour l’utilisation du panneau de contrôle ?

Non, il n’y a pas de frais supplémentaires si vous êtes déjà client Adobe Campaign.

## Identifiant de l’organisation IMS {#ims-org-id}

### Qu’est-ce qu’un identifiant de l’organisation IMS ?

Il s’agit d’un identifiant unique attribué à votre instance lorsque vous vous connectez pour la première fois à Adobe Experience Cloud. Il doit être au format : xxx@AdobeOrg.

Pour plus d’informations, voir la [documentation relative à Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).

### Où puis-je trouver mon identifiant de l’organisation IMS ?

Une méthode consiste à accéder à la [page d’accueil d’Adobe Experience Cloud](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]**. Vous trouverez votre identifiant de l’organisation IMS au bas de la section **[!UICONTROL Accès rapide]** dans Administration. Vous trouverez des informations plus détaillées dans la [documentation Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).

Vous pouvez aussi lancer **Admin Console**. Votre identifiant de l’organisation IMS est visible dans l’URL, qui se présente comme suit : https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

### Pourquoi ai-je besoin de connaître mon identifiant de l’organisation IMS ?

Pour que vous puissiez gérer les paramètres de votre instance, nous voulons nous assurer que vous obtenez les informations adéquates pour la bonne instance au cas où vous utilisez plusieurs instances pour votre entreprise.

### Que faire si je possède plusieurs identifiants de l’organisation IMS ?

Si vous avez accès à plusieurs solutions Adobe, il est possible que vous disposiez de plusieurs identifiants de l’organisation IMS. Dans ce cas, l’identifiant de l’organisation IMS correct à utiliser est celui qui est visible sous votre instance Adobe Campaign.

>[!NOTE]
>
>Si votre identifiant de l’organisation IMS est le même pour Adobe Campaign et Adobe Analytics, c’est une excellente nouvelle. En effet, un même identifiant de l’organisation IMS est nécessaire pour Analytics et Campaign si vous prévoyez d’intégrer les solutions afin de tirer parti des cas pratiques complexes tels que l’abandon du panier d’achat (pour AA + AC).
>
>Si vous avez deux identifiants d’organisation IMS différents pour Adobe Campaign et Adobe Analytics, contactez l’assistance clientèle pour qu’ils soient harmonisés.

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
