---
title: Renouvellement du certificat SSL d’un sous-domaine
description: Découvrez comment renouveler les certificats SSL de vos sous-domaines
translation-type: ht
source-git-commit: f08b0e68cf0a208b1385052510c06ca1eb679e63

---


# Renouvellement du certificat SSL d’un sous-domaine {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="[!CONTEXTUALHELP]
>id=&quot;cp_add_ssl_certificate&quot;
>title=&quot;Ajouter un certificat SSL&quot;
>abstract=&quot;Pour ajouter un certificat SSL, vous devez générer une demande de signature de certificat (CSR), acheter le certificat SSL pour vos sous-domaines et installer le pack du certificat.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/fr-FR/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr&quot; text=&quot;Génération d’une demande de signature de certificat (CSR)&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/fr-FR/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate&quot; text=&quot;Installer un certificat SSL&quot;"
>abstract="[!IMPORTANT]"
>additional-url="La délégation de sous-domaine depuis le panneau de contrôle est disponible en version bêta et sujette à de fréquentes mises à jour et modifications sans préavis." text="À propos du renouvellement des certificats {#about-certificate-renewal-process}"
>additional-url="La procédure de renouvellement des certificats SSL comprend 3 étapes :" text="**Génération de la demande de signature de certificat (CSR)**
L’Assistance clientèle Adobe génère une demande de signature de certificat pour vous. Vous devrez fournir certaines informations nécessaires à la génération de la demande de signature de certificat (telles que le nom commun, le nom et l’adresse de l’organisation, etc.)."

>**Achat du certificat SSL**
Une fois la demande de signature de certificat générée, vous pouvez la télécharger et l’utiliser pour acheter le certificat SSL auprès de l’autorité de certification approuvée par votre entreprise.
>
>**Installation du certificat SSL**
Une fois le certificat SSL acheté, vous pouvez l’installer sur le sous-domaine souhaité.

## [!NOTE]

Le renouvellement des certificats SSL depuis le panneau de contrôle est disponible uniquement pour les **sous-domaines entièrement délégués**.

1. Génération d’une demande de signature de certificat (CSR) {#generating-csr}**
1. [!CONTEXTUALHELP]
>id=&quot;cp_generate_csr&quot;
>title=&quot;Générer une demande de signature de certificat (CSR)&quot;
>abstract=&quot;La demande de signature de certificat doit être générée pour l’instance et les sous-domaines que vous envisagez de sécuriser avant d’acheter un certificat.&quot;**
1. [!CONTEXTUALHELP]
>id=&quot;cp_select_subdomains&quot;
>title=&quot;Sélectionner les sous-domaines pour votre CSR&quot;
>abstract=&quot;Vous pouvez choisir d’inclure tous les sous-domaines ou uniquement des sous-domaines spécifiques dans votre demande de signature de certificat. Seuls les sous-domaines sélectionnés seront certifiés par le biais du certificat SSL acheté.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/fr-FR/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr&quot; text=&quot;Génération d’une demande de signature de certificat (CSR)&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/fr-FR/control-panel/using/subdomains-and-certificates/subdomains-branding.html&quot; text=&quot;À propos de la marque des sous-domaines&quot;**

>[!NOTE]Pour générer une demande de signature de certificat (CSR), procédez comme suit :
>
>Dans la carte **[!UICONTROL Sous-domaines et certificats]**, sélectionnez l’instance voulue, puis cliquez sur le bouton **[!UICONTROL Gérer le certificat]**.**

## ![](assets/renewal1.png)

>[!CONTEXTUALHELP]
>id="cp_generate_csr"
>title="Sélectionnez **[!UICONTROL Générer une demande de signature de certificat]**, puis cliquez sur **[!UICONTROL Suivant]** pour lancer l’assistant qui vous guidera tout au long du processus de génération de la demande de signature de certificat."
>abstract="![](assets/renewal2.png)"

>[!CONTEXTUALHELP]
>id="cp_select_subdomains"
>title="Un formulaire s&#39;affiche contenant tous les détails nécessaires à la génération de la demande de signature de certificat."
>abstract="Veillez à renseigner précisément les informations demandées, faute de quoi il est possible que le certificat ne soit pas renouvelé (contactez votre équipe interne et les équipes de sécurité et informatique si nécessaire), puis cliquez sur **[!UICONTROL Suivant]**."
>additional-url="**[!UICONTROL Organisation]** : nom officiel de l’organisation." text="**[!UICONTROL Unité d’organisation]** : unité associée au sous-domaine (exemple : marketing, informatique)."
>additional-url="**[!UICONTROL Instance]** (prérenseigné) : URL de l’instance Campaign associée au sous-domaine." text="![](assets/renewal3.png)"

Sélectionnez les sous-domaines à inclure dans le fichier CSR, puis cliquez sur **[!UICONTROL OK]**.

1. ![](assets/renewal4.png)]******

   Les sous-domaines sélectionnés s’affichent dans la liste. Pour chacun d’eux, sélectionnez les sous-domaines à inclure, puis cliquez sur **[!UICONTROL Suivant]**.

1. ![](assets/renewal5.png)]******

   Un résumé des sous-domaines à inclure dans le fichier CSR s’affiche. Cliquez sur **[!UICONTROL Soumettre]** pour confirmer votre requête.

1. ![](assets/renewal6.png)

   Le fichier .csr correspondant à votre sélection est généré et téléchargé automatiquement. Vous pouvez désormais l’utiliser pour acheter le certificat SSL auprès de l’autorité de certification approuvée par votre société.****

   * [!NOTE]]**
   * **[!UICONTROL Si le fichier CSR n’est pas enregistré/téléchargé, il sera perdu et vous devrez le générer de nouveau.]**
   * Achat d’un certificat avec la demande de signature de certificat {#purchasing-certificate}]**
   ![](assets/renewal3.png)Après obtention d’une demande de signature de certificat via le panneau de contrôle, achetez un certificat SSL auprès d’une autorité de certification approuvée par votre société.

1. Installation du certificat SSL {#installing-ssl-certificate}]**

   [!CONTEXTUALHELP]
>id=&quot;cp_install_ssl_certificate&quot;
>title=&quot;Installer le certificat SSL&quot;
>abstract=&quot;Installez le certificat SSL que vous avez acheté auprès de l’autorité de certification approuvée par votre entreprise.&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/fr-FR/control-panel/using/subdomains-and-certificates/subdomains-branding.html&quot; text=&quot;À propos de la marque des sous-domaines&quot;

1. Une fois un certificat SSL acheté, vous pouvez l’installer sur votre instance. Avant de poursuivre, prenez connaissance des prérequis suivants :****

   ![](assets/renewal5.png)La demande de signature de certificat (CSR) doit avoir été générée depuis le panneau de contrôle. Sinon, vous ne pourrez pas installer le certificat depuis le panneau de contrôle.

1. La demande de signature de certificat (CSR) doit correspondre au sous-domaine qui a été délégué à Adobe. Par exemple, elle ne peut pas contenir d’autres sous-domaines que celui qui a été délégué.****

   ![](assets/renewal6.png)La date du certificat doit être celle en cours. Il n’est pas possible d’installer des certificats avec des dates dans le futur ou ayant expiré (les dates de début et de fin doivent être valides).

1. Le certificat doit être émis par une autorité de certification approuvée telle que Comodo, DigiCert, GoDaddy, etc.

   >[!NOTE]La taille du certificat doit être de 2 048 bits et l’algorithme doit être de type RSA.
   >
   >Le certificat doit être au format X.509 PEM.

## Les certificats SAN sont pris en charge.{#purchasing-certificate}

Les certificats génériques ne sont pas pris en charge.

## Le fichier ZIP ou le certificat ne doit pas être protégé par mot de passe.{#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id="cp_install_ssl_certificate"
>title="Le fichier ZIP ne doit contenir que les éléments suivants, de préférence dans des fichiers séparés :"
>abstract="Certificat d’entité finale."
>additional-url="Chaîne de certificats intermédiaires (organisée dans le bon ordre)." text="Certificat racine (facultatif)."

Pour installer le certificat, procédez comme suit :

* Dans la carte **[!UICONTROL Sous-domaines et certificats]**, sélectionnez l’instance voulue, puis cliquez sur le bouton **[!UICONTROL Gérer le certificat]**.
* ![](assets/renewal1.png)
* Cliquez sur **[!UICONTROL Installer un certificat SSL]**, puis sur **[!UICONTROL Suivant]** pour lancer l’assistant qui vous guidera tout au long du processus d’installation du certificat.
* ![](assets/install1.png)
* Sélectionnez le fichier .zip contenant le certificat à installer, puis cliquez sur **[!UICONTROL Soumettre]**.
* ![](assets/install2.png)
* [!NOTE]
* Le certificat sera installé sur tous les domaines/sous-domaines inclus dans la demande de signature de certificat (CSR). Aucun domaine/sous-domaine supplémentaire indiqué dans le certificat ne sera pris en compte.
* Une fois le certificat SSL installé, sa date d’expiration et son icône d’état sont mises à jour.
* **Rubriques connexes :**
   * [Ajout de certificats SSL (tutoriel vidéo)[#$tu67]
   * 
   * 

To install the certificate, follow these steps:

1. In the **[!UICONTROL Subdomains &amp; Certificates]** card, select the desired instance, then click the **[!UICONTROL Manage Certificate]** button.

   ![](assets/renewal1.png)

1. Click **[!UICONTROL Install SSL Certificate]**, then **[!UICONTROL Next]** to launch the wizard that will guide you through the certificate installation process.

   ![](assets/install1.png)

1. Select the .zip file that contains the certificate to install, then click **[!UICONTROL Submit]**.

   ![](assets/install2.png)

>[!NOTE]
>
>The certificate will get installed on all domains/subdomains included in the CSR. Any additional domain/subdomain present in the certificate will not be taken into account.

Once the SSL certificate is installed, the certificate&#39;s expiration date and status icon are updated accordingly.

**Related topics:**

* [Adding SSL certificates (tutorial video)-ERR:REF-NOT-FOUND-
* [Subdomains branding](../../subdomains-certificates/using/subdomains-branding.md)
* [Monitoring your subdomains](../../subdomains-certificates/using/monitoring-subdomains.md)