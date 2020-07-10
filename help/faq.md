---
title: FAQ sur le panneau de contrôle
description: Questions courantes relatives au panneau de contrôle
translation-type: tm+mt
source-git-commit: 35723590195ef54df42d1d1df5b37490787f8836
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 71%

---


# FAQ {#faq}

## Identifiant IMS de l&#39;organisation {#ims-org-id}

**Qu’est-ce qu’un ID d’organisation IMS ?**

Il s’agit d’un identifiant unique attribué à votre instance lorsque vous vous connectez pour la première fois à Adobe Experience Cloud. Il doit être au format : xxx@AdobeOrg.

Pour plus d’informations, voir la [documentation relative à Adobe Experience Cloud](https://marketing.adobe.com/resources/help/fr_FR/mcloud/organizations.html).

**Où puis-je trouver mon ID d’organisation IMS ?**

Une méthode consiste à accéder à la [page d’accueil d’Adobe Experience Cloud](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]**. You will find your IMS Organization ID at the bottom of Administration **[!UICONTROL Quick Access]** section. Vous trouverez des informations plus détaillées dans la [documentation Adobe Experience Cloud](https://marketing.adobe.com/resources/help/fr_FR/mcloud/organizations.html).

Vous pouvez aussi lancer **Admin Console**. Votre ID d’organisation IMS sera visible dans votre URL. Il doit se présenter comme suit : https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

**Pourquoi dois-je connaître mon ID d’organisation IMS ?**

Pour que vous puissiez gérer les paramètres de votre instance, nous voulons nous assurer que vous obtenez les informations adéquates pour la bonne instance au cas où vous utilisez plusieurs instances pour votre entreprise.

**Que se passe-t-il si j’ai plusieurs ID d’organisation IMS ?**

Vous pouvez avoir plusieurs ID d’organisation IMS si vous avez accès à plusieurs solutions Adobe. Dans ce cas, l’ID d’organisation IMS correct que vous devez utiliser est celui que vous voyez sous votre instance d’Adobe Campaign.

>[!NOTE]
>
>Si vous avez le même ID d&#39;organisation IMS pour Adobe Campaign et Adobe Analytics, c&#39;est super. La présence d&#39;un ID d&#39;organisation IMS entre Analytics et Campaign est obligatoire si vous envisagez d&#39;intégrer des solutions pour tirer parti de cas d&#39;utilisation complexes tels que l&#39;abandon de panier (pour AA + AC).
>
>Si vous disposez de différents ID d’organisation IMS pour l’Adobe Campaign et Adobe Analytics, contactez le service à la clientèle pour les aligner.

**Comment puis-je savoir si mon instance Adobe Campaign est hébergée sur AWS ?**

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

## Panneau de contrôle {#control-panel}

**Qu’est-ce que le panneau de contrôle ?**

Dans le panneau de contrôle, les administrateurs du produit peuvent gérer directement divers paramètres et contrôler la capacité des serveurs SFTP connectés à Adobe Campaign.

**Quelles sont certaines des fonctionnalités actuelles du panneau de contrôle ?**

Le panneau de contrôle vous permet de surveiller le stockage, d’ajouter des adresses IP à la liste autorisée et de gérer les clés SSH de vos serveurs SFTP en fonction de vos besoins et d’autres actions.

Pour plus d’informations, consultez la documentation relative aux actions prises en charge par le panneau de contrôle.

**Le panneau de contrôle est-il réservé à Adobe Campaign ?**

Oui, dans le panneau de contrôle, vous pouvez gérer uniquement les paramètres d’Adobe Campaign.

**Puis-je utiliser le panneau de contrôle ?**

Le panneau de contrôle n’est accessible que par les administrateurs de produit de nos clients actuels pour lesquels Adobe Campaign est hébergé sur AWS. Notez que les environnements hybrides ne sont pas encore pris en charge.

Si vous n’êtes pas administrateur, mais que vous souhaitez y accéder, veuillez contacter votre administrateur de produit pour qu’il vous ajoute en tant qu’administrateur.

**Comment puis-je accéder au panneau de contrôle ?**

Consultez les instructions détaillées dans la documentation relative à l’accès au panneau de contrôle.

**Y a-t-il des frais supplémentaires pour l’utilisation du panneau de contrôle ?**

Non, il n’y a pas de frais supplémentaires si vous êtes déjà client Adobe Campaign.
