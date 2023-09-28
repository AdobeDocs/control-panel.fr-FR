---
product: campaign
solution: Campaign
title: Ajout d’enregistrements DMARC
description: Découvrez comment ajouter un enregistrement DMARC pour un sous-domaine.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: fc026f157346253fc79bde4ce624e7efa3373af2
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---


# Ajout d’enregistrements DMARC {#dmarc}

## À propos des enregistrements DMARC {#about}

DMARC (Domain-based Message Authentication, Reporting and Conformance) est une norme de protocole d’authentification des emails qui aide les entreprises à protéger leurs domaines d’email contre les attaques de phishing et d’usurpation de nom d’utilisateur. Il vous permet de décider comment un fournisseur de messagerie doit gérer les emails qui ne parviennent pas aux contrôles SPF et DKIM, ce qui permet d’authentifier le domaine de l’expéditeur et d’empêcher toute utilisation non autorisée du domaine à des fins malveillantes.

## Limites et conditions préalables {#limitations}

* Les enregistrements SPF et DKIM sont des prérequis pour la création d’un enregistrement DMARC.
* Les enregistrements DMARC ne peuvent être ajoutés que pour les sous-domaines à l’aide de la délégation de sous-domaine complète. [En savoir plus sur les méthodes de configuration des sous-domaines](subdomains-branding.md#subdomain-delegation-methods)

## Ajout d’un enregistrement DMARC pour un sous-domaine {#add}

Pour ajouter un enregistrement DMARC pour un sous-domaine, procédez comme suit :

1. Dans la liste des sous-domaines, cliquez sur le bouton représentant des points de suspension en regard du sous-domaine souhaité, puis sélectionnez **[!UICONTROL Détails du sous-domaine]**.

1. Cliquez sur le bouton **[!UICONTROL Ajout d’un enregistrement TXT]** , puis choisissez **[!UICONTROL DMARC]** de la **[!UICONTROL Type d’enregistrement]** liste déroulante.

   ![](assets/dmarc-add.png)

1. Choisissez la **[!UICONTROL Type de stratégie]** que le serveur destinataire doit suivre en cas d&#39;échec de l&#39;un de vos emails. Les types de stratégie disponibles sont les suivants :

   * Aucun,
   * Quarantaine (emplacement du dossier spam),
   * Rejeter (bloquer l&#39;email).

   Si votre sous-domaine vient d’être configuré, nous vous recommandons de définir cette valeur sur &quot;Aucun&quot; jusqu’à ce que votre sous-domaine soit entièrement configuré et que vos emails soient envoyés correctement. Une fois que tout est correctement configuré, vous pouvez remplacer le type de stratégie par &quot;Quarantaine&quot; ou &quot;Rejeter&quot;.

   >[!NOTE]
   >
   > La création d’enregistrement BIMI n’est pas disponible avec un type de stratégie d’enregistrement DMARC défini sur &quot;Aucun&quot;.

1. Renseignez les adresses électroniques qui doivent recevoir les rapports DMARC. Lorsque l’un de vos emails échoue, les rapports DMARC sont automatiquement envoyés à l’adresse email de votre choix :

   * Les rapports DMARC d’agrégat fournissent des informations de haut niveau, telles que le nombre d’emails ayant échoué pour une période donnée.
   * Les rapports d’échec DMARC de l’autorité judiciaire fournissent des informations détaillées, telles que l’adresse IP d’où provient l’échec de l’email.

1. Par défaut, la stratégie DMARC sélectionnée est appliquée à tous les emails. Vous pouvez modifier ce paramètre afin de ne l’appliquer qu’à un pourcentage spécifique d’emails.

   Lorsque vous déployez progressivement DMARC, vous pouvez commencer avec un petit pourcentage de vos messages. À mesure que davantage de messages de votre domaine transmettent l’authentification aux serveurs de réception, mettez à jour votre enregistrement avec un pourcentage plus élevé, jusqu’à ce que vous atteigniez 100 %.

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