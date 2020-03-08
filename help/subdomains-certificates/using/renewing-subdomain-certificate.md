---
title: Renouvellement du certificat SSL d’un sous-domaine
description: Découvrez comment renouveler les certificats SSL de vos sous-domaines
translation-type: tm+mt
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451

---


# Renouvellement du certificat SSL d’un sous-domaine {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id=&quot;cp_add_ssl_certificate&quot;
>title=&quot;Ajouter certificat SSL&quot;
>abstract=&quot;Pour ajouter un certificat SSL, vous devez générer un fichier CSR, acheter le certificat SSL pour vos sous-domaines et installer le lot de certificats.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr&quot; text=&quot;Génération d’une demande de signature de certificat (CSR)&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate&quot; text=&quot;Comment installer un certificat SSL&quot;

>[!IMPORTANT]
>
>La délégation de sous-domaine depuis le panneau de contrôle est disponible en version bêta et sujette à de fréquentes mises à jour et modifications sans préavis.

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

>[!CONTEXTUALHELP]
>id=&quot;cp_generate_csr&quot;
>title=&quot;Générer CSR&quot;
>abstract=&quot;La demande de signature de certificat doit être générée pour l’instance et les sous-domaines que vous prévoyez de sécuriser avant d’acheter un certificat.&quot;

>[!CONTEXTUALHELP]
>id=&quot;cp_select_subdomains&quot;
>title=&quot;Sélectionnez les sous-domaines de votre CSR&quot;
>abstract=&quot;Vous pouvez choisir d’inclure tous les sous-domaines ou uniquement des sous-domaines spécifiques dans votre demande de signature de certificat. Seuls les sous-domaines sélectionnés seront certifiés par le biais du certificat SSL acheté.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr&quot; text=&quot;Génération d’une demande de signature de certificat (CSR)&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html&quot; text=&quot;A propos de la marque des sous-domaines&quot;

Pour générer une demande de signature de certificat (CSR), procédez comme suit :

1. Dans la **[!UICONTROL Subdomains & Certificates]** carte, sélectionnez une instance, puis cliquez sur le **[!UICONTROL Manage Certificate]** bouton.

   ![](assets/renewal1.png)

1. Select **[!UICONTROL Generate a CSR]**, then click **[!UICONTROL Next]** to launch the wizard that will guide you through the CSR generation process.

   ![](assets/renewal2.png)

1. Un formulaire s&#39;affiche contenant tous les détails nécessaires à la génération de la demande de signature de certificat.

   Make sure you fill in the requested information fully and accurately, otherwise the certificate may not be renewed (contact your internal team, Security and IT teams if necessary), then click **[!UICONTROL Next]**.

   * **[!UICONTROL Organization]**: nom officiel de l&#39;organisation.
   * **[!UICONTROL Organization Unit]**: unité liée au sous-domaine (exemple : Marketing, IT).
   * **[!UICONTROL Instance]** (prérenseigné) : URL de l’instance Campaign associée au sous-domaine.
   ![](assets/renewal3.png)

1. Sélectionnez les sous-domaines à inclure dans le fichier CSR, puis cliquez sur **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. Les sous-domaines sélectionnés s’affichent dans la liste. For each of them, select the subdomains to include, then click **[!UICONTROL Next]**.

   ![](assets/renewal5.png)

1. Un résumé des sous-domaines à inclure dans le fichier CSR s’affiche. Click **[!UICONTROL Submit]** to confirm your request.

   ![](assets/renewal6.png)

1. Le fichier .csr correspondant à votre sélection est généré et téléchargé automatiquement. Vous pouvez désormais l’utiliser pour acheter le certificat SSL auprès de l’autorité de certification approuvée par votre société.

   >[!NOTE]
   >
   >Si le fichier CSR n’est pas enregistré/téléchargé, il sera perdu et vous devrez le générer de nouveau.

## Achat d’un certificat avec la demande de signature de certificat {#purchasing-certificate}

Après obtention d’une demande de signature de certificat via le panneau de contrôle, achetez un certificat SSL auprès d’une autorité de certification approuvée par votre société.

## Installation du certificat SSL {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id=&quot;cp_install_ssl_certificate&quot;
>title=&quot;Installer le certificat SSL&quot;
>abstract=&quot;Installez le certificat SSL que vous avez acheté auprès de l’autorité de certification approuvée par votre organisation.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html&quot; text=&quot;A propos de la marque des sous-domaines&quot;

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

1. Dans la **[!UICONTROL Subdomains & Certificates]** carte, sélectionnez une instance, puis cliquez sur le **[!UICONTROL Manage Certificate]** bouton.

   ![](assets/renewal1.png)

1. Click **[!UICONTROL Install SSL Certificate]**, then **[!UICONTROL Next]** to launch the wizard that will guide you through the certificate installation process.

   ![](assets/install1.png)

1. Select the .zip file that contains the certificate to install, then click **[!UICONTROL Submit]**.

   ![](assets/install2.png)

Une fois le certificat SSL installé, sa date d’expiration et son icône d’état sont mises à jour.

**Rubriques connexes :**

* [Ajout de certificats SSL (tutoriel vidéo)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [Marque des sous-domaines](../../subdomains-certificates/using/subdomains-branding.md)
* [Surveillance de vos sous-domaines](../../subdomains-certificates/using/monitoring-subdomains.md)