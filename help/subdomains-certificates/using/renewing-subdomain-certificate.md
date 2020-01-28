---
title: Renouvellement du certificat SSL d’un sous-domaine
description: Découvrez comment renouveler les certificats SSL de vos sous-domaines
translation-type: ht
source-git-commit: 50d29d25891adc866d624888ca72e16e529ae7bf

---


# Renouvellement du certificat SSL d’un sous-domaine {#renewing-subdomains-ssl-certificates}

>[!IMPORTANT]
>
>La délégation de sous-domaine depuis le panneau de contrôle sera disponible en version bêta d&#39;ici la fin janvier. Elle sera sujette à de fréquentes mises à jour et modifications sans préavis.

## À propos du renouvellement des certificats {#about-certificate-renewal-process}

La procédure de renouvellement des certificats SSL comprend 3 étapes :

1. **Génération de la demande de signature de certificat (CSR)**
L’Assistance clientèle Adobe génère une demande de signature de certificat pour vous. Vous devrez fournir certaines informations nécessaires à la génération de la demande de signature de certificat (telles que le nom commun, le nom et l’adresse de l’organisation, etc.).
1. **Achat du certificat SSL**
Une fois la demande de signature de certificat générée, vous pouvez la télécharger et l’utiliser pour acheter le certificat SSL auprès de l’autorité de certification approuvée par votre entreprise.
1. **Installation du certificat SSL**
Une fois le certificat SSL acheté, vous pouvez l’installer sur le sous-domaine souhaité.

>[!NOTE]
>
>Le renouvellement des certificats SSL depuis le panneau de contrôle est disponible uniquement pour les **sous-domaines entièrement délégués**.

## Génération d’une demande de signature de certificat (CSR) {#generating-csr}

Pour générer une demande de signature de certificat (CSR), procédez comme suit :

1. Dans la carte **[!UICONTROL Sous-domaines et certificats]**, sélectionnez l’instance voulue, puis cliquez sur le bouton**[!UICONTROL  Gérer le certificat]**.

   ![](assets/renewal1.png)

1. Sélectionnez **[!UICONTROL Générer une demande de signature de certificat]**, puis cliquez sur**[!UICONTROL  Suivant]** pour lancer l’assistant qui vous guidera tout au long du processus de génération de la demande de signature de certificat.

   ![](assets/renewal2.png)

1. Un formulaire s&#39;affiche contenant tous les détails nécessaires à la génération de la demande de signature de certificat.

   Veillez à renseigner précisément les informations demandées, faute de quoi il est possible que le certificat ne soit pas renouvelé (contactez votre équipe interne et les équipes de sécurité et informatique si nécessaire), puis cliquez sur **[!UICONTROL Suivant]**.

   * **[!UICONTROL Organisation]** : nom officiel de l’organisation.
   * **[!UICONTROL Unité d’organisation]** : unité associée au sous-domaine (exemple : marketing, informatique).
   * **[!UICONTROL Instance]** (prérenseigné) : URL de l’instance Campaign associée au sous-domaine.
   ![](assets/renewal3.png)

1. Sélectionnez les sous-domaines à inclure dans le fichier CSR, puis cliquez sur **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. Les sous-domaines sélectionnés s’affichent dans la liste. Pour chacun d’eux, sélectionnez les sous-domaines à inclure, puis cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/renewal5.png)

1. Un résumé des sous-domaines à inclure dans le fichier CSR s’affiche. Cliquez sur **[!UICONTROL Soumettre]**pour confirmer votre requête.

   ![](assets/renewal6.png)

1. Le fichier .csr correspondant à votre sélection est généré et téléchargé automatiquement. Vous pouvez désormais l’utiliser pour acheter le certificat SSL auprès de l’autorité de certification approuvée par votre société.

   >[!NOTE]
   >
   >Si le fichier CSR n’est pas enregistré/téléchargé, il sera perdu et vous devrez le générer de nouveau.

## Achat d’un certificat avec la demande de signature de certificat {#purchasing-certificate}

Après obtention d’une demande de signature de certificat via le panneau de contrôle, achetez un certificat SSL auprès d’une autorité de certification approuvée par votre société.

## Installation du certificat SSL {#installing-ssl-certificate}

Une fois un certificat SSL acheté, vous pouvez l’installer sur votre instance. Avant de poursuivre, prenez connaissance des prérequis suivants :

* La demande de signature de certificat (CSR) doit avoir été générée depuis le panneau de contrôle. Sinon, vous ne pourrez pas installer le certificat depuis le panneau de contrôle.
* La demande de signature de certificat (CSR) doit correspondre au sous-domaine qui a été délégué à Adobe. Par exemple, elle ne peut pas contenir d’autres sous-domaines que celui qui a été délégué.
* La date du certificat doit être celle en cours. Il n’est pas possible d’installer des certificats avec des dates dans le futur ou ayant expiré (les dates de début et de fin doivent être valides).
* Le certificat doit être émis par une autorité de certification approuvée telle que Comodo, DigiCert, GoDaddy, etc.
* La taille du certificat doit être de 2 048 bits et l’algorithme doit être de type RSA.
* Le certificat doit être au format X.509 PEM.
* Les certificats SAN sont pris en charge.
* Les certificats génériques ne sont pas pris en charge.
* Le fichier ZIP ou le certificat ne doit pas être protégé par mot de passe.
* Le fichier ZIP ne doit contenir que les éléments suivants, de préférence dans des fichiers séparés :
   * Certificat d’entité finale.
   * Chaîne de certificats intermédiaires (organisée dans le bon ordre).
   * Certificat racine (facultatif).

Pour installer le certificat, procédez comme suit :

1. Dans la carte **[!UICONTROL Sous-domaines et certificats]**, sélectionnez l’instance voulue, puis cliquez sur le bouton**[!UICONTROL  Gérer le certificat]**.

   ![](assets/renewal1.png)

1. Cliquez sur **[!UICONTROL Installer un certificat SSL]**, puis sur**[!UICONTROL  Suivant]** pour lancer l’assistant qui vous guidera tout au long du processus d’installation du certificat.

   ![](assets/install1.png)

1. Sélectionnez le fichier .zip contenant le certificat à installer, puis cliquez sur **[!UICONTROL Soumettre]**.

   ![](assets/install2.png)

Une fois le certificat SSL installé, sa date d’expiration et son icône d’état sont mises à jour.
