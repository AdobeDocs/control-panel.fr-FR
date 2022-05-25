---
product: campaign
solution: Campaign
title: Ajouter des instances MID/RT (modèle hybride)
description: Découvrez comment ajouter des instances MID/RT au Panneau de Contrôle avec le modèle d’hébergement hybride.
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: 2458263ef5981a16d983912b498e320501df7889
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Ajouter des instances MID/RT (modèle hybride)

>[!CONTEXTUALHELP]
>id="cp_externalaccounts"
>title="Comptes externes"
>abstract="Dans cet écran, les clients disposant d’un modèle d’hébergement hybride peuvent fournir l’URL de leur instance MID/RT configurée dans l’instance marketing en Panneau de Contrôle, afin d’exploiter les fonctionnalités de Panneau de Contrôle."

Panneau de Contrôle permet aux clients disposant d’un modèle d’hébergement hybride d’exploiter des fonctionnalités de Panneau de Contrôle spécifiques. Pour ce faire, ils doivent fournir l’URL de l’instance MID/RT configurée dans leur instance marketing en Panneau de Contrôle.

Pour plus d’informations sur les modèles d’hébergement, reportez-vous à la [documentation de Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html?lang=fr).

## Ajout d’une instance MID/RT {#add}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="URL"
>abstract="URL de l&#39;instance, disponible dans la console cliente de Campaign dans le menu Administration > Plateforme > Comptes externes ."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="Opérateur"
>abstract="Identifiant de l’opérateur fourni après la mise en service initiale par l’administrateur Adobe."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="Mot de passe"
>abstract="Mot de passe de l&#39;opérateur fourni après la mise en service initiale par l&#39;administrateur Adobe."

Les clients hybrides doivent se connecter à Panneau de Contrôle par le biais d’Experience Cloud. Lorsque vous accédez au panneau de contrôle pour la première fois, seules deux vignettes s’afficheront sur la page d’accueil.

![](assets/hybrid-homepage.png)

>[!NOTE]
>
>Si vous rencontrez des problèmes pour accéder au panneau de contrôle, il est probable que votre instance marketing ne soit pas encore mappée avec votre ID d’organisation. Contactez l’assistance clientèle pour terminer cette configuration pour continuer. Une fois la connexion établie, la page d’accueil du Panneau de Contrôle s’affiche.

Pour pouvoir accéder aux fonctionnalités du panneau de contrôle, vous devez fournir les informations de votre instance MID/RT dans la vignette des **[!UICONTROL Paramètres des instances]**. Pour ce faire, suivez les étapes ci-après.

1. Dans la vignette **[!UICONTROL Paramètres des instances]**, sélectionnez l’onglet **[!UICONTROL Comptes externes]**.

1. Sélectionnez l’instance marketing désirée dans la liste déroulante, puis cliquez sur **[!UICONTROL Ajouter une nouvelle URL]**.

   ![](assets/external-account-addbutton.png)

1. Fournissez des informations sur l’instance MID/RT à ajouter.

   ![](assets/external-account-add.png)

   * **[!UICONTROL URL]**: URL de l’instance, qui se trouve dans la console cliente de Campaign dans le **[!UICONTROL Administration]** > **[!UICONTROL Plateforme]** > **[!UICONTROL Comptes externes]** .

      ![](assets/external-account-url.png)

   * **[!UICONTROL Opérateur]**/**[!UICONTROL Mot de passe]** : les informations d’identification de l’opérateur fournies après l’approvisionnement initial par Adobe Admin.

      >[!NOTE]
      >
      >Si ces informations ne sont pas disponibles, contactez l’assistance clientèle.

1. Cliquez sur **[!UICONTROL Enregistrer]** pour confirmer.

Lors de l’ajout d’une URL MID/RT, un processus asynchrone est déclenché pour valider l’exactitude des URL. Ce processus peut prendre quelques minutes. Tant que l’URL de l’instance MID/RT n’est pas validée, la tâche est en attente. Une fois la validation terminée, vous pouvez accéder aux principales fonctionnalités du panneau de contrôle.

![](assets/external-account-pending.png)

Vous pouvez supprimer ou désactiver l’URL d&#39;une instance MID/RT à tout moment en la sélectionnant dans la liste.

![](assets/external-account-edit.png)

Notez que vous pouvez surveiller toute action effectuée dans la variable **[!UICONTROL Comptes externes]** de l’onglet sur une URL d’instance MID/RT à partir de **[!UICONTROL Logs de traitement]**:

![](assets/external-account-logs.png)

## Fonctionnalités disponibles pour les clients hybrides {#capabilities}

Une fois qu’une instance MID/RT est ajoutée au Panneau de Contrôle, vous pouvez exploiter les fonctionnalités répertoriées ci-dessous :

* [Surveiller les contacts principaux et les événements](../../service-events/service-events.md)
* [Afficher les détails de votre instance](../../instances-settings/using/instance-details.md),
* [Ajout d’adresses IP à la liste autorisée](../../instances-settings/using/ip-allow-listing-instance-access.md) (pour les instances RT),
* [Afficher des informations sur les sous-domaines délégués](../../subdomains-certificates/using/monitoring-subdomains.md),
* [Afficher des informations sur les certificats SSL](../../subdomains-certificates/using/monitoring-ssl-certificates.md).