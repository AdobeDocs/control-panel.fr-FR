---
product: campaign
solution: Campaign
title: Ajout d’enregistrements DMARC
description: Découvrez comment ajouter un enregistrement DMARC pour un sous-domaine.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2ca66983-5beb-495a-9639-a31905500cff
source-git-commit: 64ea5e26786eea107983ee5025025c81334b0a91
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Ajout d’enregistrements DMARC {#dmarc}

## À propos des enregistrements DMARC {#about}

DMARC (Domain-based Message Authentication, Reporting and Conformance) est une norme de protocole d’authentification des emails qui aide les entreprises à protéger leurs domaines d’email contre les attaques de phishing et d’usurpation de nom d’utilisateur. Il vous permet de décider comment un fournisseur de messagerie doit gérer les emails qui ne parviennent pas aux contrôles SPF et DKIM, ce qui permet d’authentifier le domaine de l’expéditeur et d’empêcher toute utilisation non autorisée du domaine à des fins malveillantes.

Des informations détaillées sur la mise en oeuvre DMARC sont disponibles dans la section [Guide des bonnes pratiques de délivrabilité des Adobes](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html)

## Limites et conditions préalables {#limitations}

* Les enregistrements SPF et DKIM sont des prérequis pour la création d’un enregistrement DMARC.
* Les enregistrements DMARC ne peuvent être ajoutés que pour les sous-domaines à l’aide de la délégation de sous-domaine complète. [En savoir plus sur les méthodes de configuration des sous-domaines](subdomains-branding.md#subdomain-delegation-methods)

## Ajout d’un enregistrement DMARC pour un sous-domaine {#add}

Pour ajouter un enregistrement DMARC pour un sous-domaine, procédez comme suit :

1. Dans la liste des sous-domaines, cliquez sur le bouton représentant des points de suspension en regard du sous-domaine souhaité, puis sélectionnez **[!UICONTROL Détails du sous-domaine]**.

1. Cliquez sur le bouton **[!UICONTROL Ajout d’un enregistrement TXT]** , puis choisissez **[!UICONTROL DMARC]** de la **[!UICONTROL Type d’enregistrement]** liste déroulante.

   ![](assets/dmarc-add.png)

1. Choisissez la **[!UICONTROL Type de stratégie]** que le serveur destinataire doit suivre en cas d&#39;échec de l&#39;un de vos emails. Les types de stratégie disponibles sont les suivants :

   * **[!UICONTROL Aucun]**,
   * **[!UICONTROL Quarantaine]** (placement de dossier de spam),
   * **[!UICONTROL Rejeter]** (bloquer l’email).

   Il est recommandé de déployer lentement la mise en oeuvre DMARC en réaffectant votre stratégie DMARC de p=none à p=quarantine, puis de p=reject lorsque vous acquérez une compréhension DMARC de l’impact potentiel de DMARC.

   * **Étape 1 :** Analysez les commentaires que vous recevez et utilisez (p=none), qui indique au destinataire d’effectuer aucune action contre les messages qui ne parviennent pas à s’authentifier, tout en envoyant des rapports par e-mail à l’expéditeur. En outre, passez en revue et corrigez les problèmes liés à SPF/DKIM si les messages légitimes échouent à l’authentification.

   * **Étape 2 :** Déterminez si SPF et DKIM sont harmonisés et passent une authentification pour tous les emails légitimes, puis déplacez la stratégie vers (p=quarantine), ce qui indique au serveur de messagerie de réception de mettre en quarantaine les emails qui ne parviennent pas à s’authentifier (cela signifie généralement placer ces messages dans le dossier spam). Si la stratégie est définie pour être mise en quarantaine, il est recommandé de commencer avec un petit pourcentage de vos emails.

   * **Étape 3 :** Ajustez la stratégie à (p=rejets). REMARQUE : Utilisez cette politique avec précaution et déterminez si elle convient à votre entreprise. La stratégie p= rejet indique au destinataire de refuser complètement (rebond) tout courrier électronique pour le domaine qui échoue à l’authentification. Lorsque cette stratégie est activée, seul le courrier électronique vérifié comme authentifié à 100 % par votre domaine aura une chance d’être envoyé en boîte de réception.

   >[!NOTE]
   >
   > La création d’enregistrement BIMI n’est pas disponible avec un type de stratégie d’enregistrement DMARC défini sur &quot;Aucun&quot;.

1. Renseignez les adresses électroniques qui doivent recevoir les rapports DMARC. Lorsque l’un de vos emails échoue, les rapports DMARC sont automatiquement envoyés à l’adresse email de votre choix :

   * Les rapports DMARC d’agrégat fournissent des informations de haut niveau, telles que le nombre d’emails ayant échoué pour une période donnée.
   * Les rapports d’échec DMARC de l’autorité judiciaire fournissent des informations détaillées, telles que l’adresse IP d’où provient l’échec de l’email.

1. Si la stratégie DMARC est définie sur &quot;Aucun&quot;, saisissez un pourcentage applicable à 100 % des emails.

   Si la stratégie est définie sur &quot;Rejeter&quot; ou &quot;Quarantaine&quot;, il est recommandé de commencer avec un petit pourcentage de vos emails. À mesure que davantage de courriers électroniques de votre domaine transmettent l’authentification aux serveurs de réception, mettez à jour votre enregistrement lentement avec un pourcentage plus élevé.

   >[!NOTE]
   >
   >Si votre domaine utilise l’IMI, votre stratégie DMARC doit avoir une valeur en pourcentage de 100 %. BIMI ne prend pas en charge les stratégies DMARC avec cette valeur définie sur moins de 100 %.

   ![](assets/dmarc-add2.png)

1. Les rapports DMARC sont envoyés toutes les 24 heures. Vous pouvez modifier la fréquence d&#39;envoi des rapports dans la variable **[!UICONTROL Intervalle de création de rapports]** champ . L’intervalle minimum autorisé est de 1 heure, tandis que la valeur maximale autorisée est de 2 190 heures (soit 3 mois).

1. Dans le **SPF** et **[!UICONTROL Alignement de l’identifiant DKIM]** , indiquez à quel point les serveurs de destinataires doivent être stricts lors de la vérification des authentifications SPF et DKIM pour un email.

   * **[!UICONTROL Relaxage]** mode : le serveur accepte l’authentification même si l’email est envoyé à partir d’un sous-domaine,
   * **[!UICONTROL Strict]** Le mode accepte l’authentification uniquement lorsque le domaine de l’expéditeur correspond exactement à un domaine SPF et DKIM.

   Disons que nous travaillons avec le `http://www.luma.com` domaine. En mode &quot;Relaxé&quot;, les emails provenant de `marketing.luma.com` Le sous-domaine sera autorisé par le serveur, mais il sera rejeté en mode &quot;Strict&quot;.

1. Cliquez sur **[!UICONTROL Ajouter]** pour confirmer la création de l’enregistrement DMARC.

Une fois la création d’enregistrement DMARC traitée (environ 5 minutes), elle s’affiche dans l’écran de détails des sous-domaines. [Découvrez comment surveiller les enregistrements TXT pour vos sous-domaines](gs-txt-records.md#monitor)
