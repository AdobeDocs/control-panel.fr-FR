---
product: campaign
solution: Campaign
title: Renouvellement du certificat SSL d’un sous-domaine
description: Découvrez comment renouveler les certificats SSL de vos sous-domaines
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: b31853a861aad7beb5b639f0fa22e821e8e25e19
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Générer une demande de signature de certificat {#generating-csr}

>[!CONTEXTUALHELP]
>id="cp_generate_csr"
>title="Génération dʼune demande de signature de certificat"
>abstract="La demande de signature de certificat doit être générée pour l’instance et les sous-domaines que vous envisagez de sécuriser avant d’acheter un certificat."

>[!CONTEXTUALHELP]
>id="cp_select_subdomains"
>title="Sélectionner les sous-domaines pour votre CSR"
>abstract="Vous pouvez choisir d’inclure tous les sous-domaines ou uniquement des sous-domaines spécifiques dans votre demande de signature de certificat. Seuls les sous-domaines sélectionnés seront certifiés par le biais du certificat SSL acheté."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=fr" text="À propos de la marque des sous-domaines"

## Génération de la demande de signature de certificat {#generate}

Pour générer une demande de signature de certificat (CSR), procédez comme suit :

1. Dans la carte **[!UICONTROL Sous-domaines et certificats]**, sélectionnez l’instance voulue, puis cliquez sur le bouton **[!UICONTROL Gérer le certificat]**.

   ![](assets/renewal1.png)

1. Sélectionnez **[!UICONTROL 1 - Génération d’une demande de signature de certificat]**, puis cliquez sur **[!UICONTROL Suivant]** pour lancer l’assistant qui vous guidera tout au long de ce processus.

   ![](assets/renewal2.png)

1. Un formulaire s’affiche contenant tous les détails nécessaires à la génération de la demande de signature de certificat.

   Veillez à renseigner précisément les informations demandées, faute de quoi il est possible que le certificat ne soit pas renouvelé (contactez votre équipe interne et les équipes de sécurité et informatique si nécessaire), puis cliquez sur **[!UICONTROL Suivant]**.

   * **[!UICONTROL Organisation]** : nom officiel de l’organisation.
   * **[!UICONTROL Unité d’organisation]** : unité associée au sous-domaine (exemple : marketing, informatique).
   * **[!UICONTROL Instance]** (prérenseigné) : URL de l’instance Campaign associée au sous-domaine.
   * **[!UICONTROL Nom commun]**: si le nom commun est sélectionné par défaut, vous pouvez sélectionner l’un des sous-domaines si nécessaire.

   ![](assets/renewal3.png)

1. Sélectionnez les sous-domaines à inclure dans le fichier CSR, puis cliquez sur **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. Les sous-domaines sélectionnés s’affichent dans la liste. Pour chacun d’eux, sélectionnez les sous-domaines à inclure, puis cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/renewal5.png)

1. Un résumé des sous-domaines à inclure dans le fichier CSR s’affiche. Cliquez sur **[!UICONTROL Soumettre]** pour confirmer votre requête.

   ![](assets/renewal6.png)

   >[!NOTE]
   >
   >Le **[!UICONTROL Copie du contenu CSR]** permet de copier toutes les informations relatives à la demande de signature de certificat (ID d’organisation, instance, nom de l’organisation, nom commun, sous-domaines inclus, etc.).

1. Le fichier .csr correspondant à votre sélection est généré et téléchargé automatiquement. Vous pouvez désormais l’utiliser pour acheter le certificat SSL auprès de l’autorité de certification approuvée par votre société. Si vous devez télécharger à nouveau la demande de signature de certificat, suivez les étapes présentées dans la section [cette section](#download).

Une fois votre demande de signature de certificat générée et téléchargée, vous pouvez l’utiliser pour acheter un certificat SSL auprès d’une autorité de certification approuvée par votre organisation.

Une fois le certificat SSL acheté, vous pourrez l’installer sur votre instance pour sécuriser votre sous-domaine. [En savoir plus](install-ssl-certificate.md)

## Téléchargement de la demande de signature de certificat {#download}

Pour acheter un certificat SSL, vous devez d’abord télécharger la demande de signature de certificat. La demande de signature de certificat est automatiquement téléchargée après sa génération. Vous pouvez également le télécharger à nouveau à tout moment à partir des logs de traitement :

1. Dans le **[!UICONTROL Logs de traitement]**, sélectionnez la variable **[!UICONTROL Terminé]** puis filtrez la liste afin d’afficher les tâches liées à la gestion des sous-domaines.

   ![](assets/renewal-download.png)

1. Ouvrez la tâche correspondant à la génération du CSR, puis cliquez sur le bouton **[!UICONTROL Télécharger]** pour obtenir le fichier .csr.

   ![](assets/renewal-download-button.png)
