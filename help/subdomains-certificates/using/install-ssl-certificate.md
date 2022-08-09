---
product: campaign
solution: Campaign
title: Renouvellement du certificat SSL d’un sous-domaine
description: Découvrez comment renouveler les certificats SSL de vos sous-domaines
feature: Control Panel
role: Architect
level: Experienced
exl-id: af440b5d-1d21-44fb-831f-f2bdd6011b82
source-git-commit: 9be5a3ae48dccf74f509aa95fee29bbfdafddcdf
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 100%

---

# Installer le certificat SSL {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id="cp_install_ssl_certificate"
>title="Installation du certificat SSL"
>abstract="Installez le certificat SSL que vous avez acheté auprès de lʼautorité de certification approuvée par votre organisation."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=fr" text="À propos de la marque des sous-domaines"

Une fois un certificat SSL acheté, vous pouvez l’installer sur votre instance. Avant de poursuivre, prenez connaissance des prérequis suivants :

* La demande de signature de certificat (CSR) doit avoir été générée depuis le Panneau de contrôle. Sinon, vous ne pourrez pas installer le certificat depuis le Panneau de contrôle.
* La demande de signature de certificat (CSR) doit correspondre au sous-domaine qui a été configuré pour fonctionner avec Adobe. Par exemple, il ne peut pas contenir plus de sous-domaines que celui qui a été configuré.
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

1. Dans la carte **[!UICONTROL Sous-domaines et certificats]**, sélectionnez l’instance voulue, puis cliquez sur le bouton **[!UICONTROL Gérer le certificat]**.

   ![](assets/renewal1.png)

1. Sélectionnez **[!UICONTROL 3 - Installation de l’ensemble de certificats]**, puis cliquez sur **[!UICONTROL Suivant]** pour lancer l’assistant qui vous guidera tout au long du processus d’installation du certificat.

   ![](assets/install1.png)

1. Sélectionnez le fichier .zip contenant le certificat à installer, puis cliquez sur **[!UICONTROL Soumettre]**.

   ![](assets/install2.png)

>[!NOTE]
>
>Le certificat sera installé sur tous les domaines/sous-domaines inclus dans la demande de signature de certificat (CSR). Aucun domaine/sous-domaine supplémentaire indiqué dans le certificat ne sera pris en compte.

Une fois le certificat SSL installé, sa date d’expiration et son icône d’état sont mises à jour.
