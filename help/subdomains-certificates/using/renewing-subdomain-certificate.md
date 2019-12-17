---
title: Renouvellement du certificat SSL d’un sous-domaine
description: Découvrez comment renouveler les certificats SSL de vos sous-domaines
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Renouvellement du certificat SSL d’un sous-domaine {#renewing-subdomains-ssl-certificates}

## A propos du renouvellement des certificats {#about-certificate-renewal-process}

Le processus de renouvellement du certificat SSL comprend 3 étapes, toutes exécutées directement à partir du Panneau de configuration :

1. **Génération de la demande de signature de certificat (CSR) Le service à la clientèle** Adobe génère une demande de signature de certificat pour vous. Vous devrez fournir certaines informations nécessaires à la génération de la demande de signature de certificat (telles que le nom commun, le nom et l’adresse de l’organisation, etc.).
1. **Achat du certificat** SSL Une fois le fichier CSR généré, vous pouvez le télécharger et l’utiliser pour acheter le certificat SSL auprès de l’autorité de certification approuvée par votre société.
1. **Installation du certificat** SSL Une fois le certificat SSL acheté, vous pouvez l’installer sur le sous-domaine souhaité.

## Génération d’une demande de signature de certificat (CSR) {#generating-csr}

Pour générer une demande de signature de certificat (CSR), procédez comme suit :

1. Dans la carte **[!UICONTROL Sous-domaines et certificats]**, sélectionnez une instance, puis cliquez sur le bouton**[!UICONTROL  Gérer le certificat]** .

   ![](assets/renewal1.png)

1. Sélectionnez **[!UICONTROL Générer une CSR]**, puis cliquez sur**[!UICONTROL  Suivant]** pour lancer l’assistant qui vous guidera tout au long du processus de génération de CSR.

   ![](assets/renewal2.png)

1. Un formulaire s’affiche, avec tous les détails nécessaires pour générer votre CSR.

   Make sure you fill in the requested information fully and accurately (contact your internal team, Security and IT teams if necessary), then click **[!UICONTROL Next]**.

   * **[!UICONTROL Organisation]**:
   * **[!UICONTROL Unité d’organisation]**:
   * **[!UICONTROL Instance]**: URL de l’instance Campaign associée au sous-domaine.
   ![](assets/renewal3.png)

1. Sélectionnez les sous-domaines à inclure dans le fichier CSR, puis cliquez sur **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. Les sous-domaines sélectionnés s’affichent dans la liste. Pour chacun d’eux, sélectionnez les sous-domaines à inclure, puis cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/renewal5.png)

1. Un résumé des sous-domaines à inclure dans le fichier CSR s’affiche. Cliquez sur **[!UICONTROL Envoyer]**pour confirmer votre requête.

   ![](assets/renewal6.png)

1. Le fichier .csr correspondant à votre sélection est généré et téléchargé automatiquement. Vous pouvez désormais l’utiliser pour acheter le certificat SSL auprès de l’autorité de certification approuvée par votre société.

## Achat d’un certificat avec le CSR {#purchasing-certificate}

Après avoir obtenu une demande de signature de certificat CSR auprès du Panneau de configuration, achetez un certificat SSL auprès d’une autorité de certification approuvée par votre organisation.

## Installation du certificat SSL {#installing-ssl-certificate}

Une fois un certificat SSL acheté, procédez comme suit pour l’installer sur votre instance.

1. Dans la carte **[!UICONTROL Sous-domaines et certificats]**, sélectionnez une instance, puis cliquez sur le bouton**[!UICONTROL  Gérer le certificat]** .

   ![](assets/renewal1.png)

1. Cliquez sur **[!UICONTROL Installer le certificat]**SSL, puis sur**[!UICONTROL  Suivant]** pour lancer l’assistant qui vous guidera tout au long du processus d’installation du certificat.

   ![](assets/install1.png)

1. Sélectionnez le fichier .zip contenant le certificat à installer, puis cliquez sur **[!UICONTROL Envoyer]**.

   ![](assets/install2.png)
