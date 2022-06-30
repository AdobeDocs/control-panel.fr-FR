---
product: campaign
solution: Campaign
title: Renouvellement du certificat SSL d’un sous-domaine
description: Découvrez comment renouveler les certificats SSL de vos sous-domaines
feature: Control Panel
role: Architect
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: 5a5ac1a604fe5bdce07479ff84184abdb2e0ddba
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Renouvellement d’un certificat SSL {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="Renouvellement du certificat SSL"
>abstract="Pour renouveler un certificat SSL, vous devez générer une demande de signature de certificat (CSR), acheter le certificat SSL pour vos sous-domaines et installer l’ensemble de certificats."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html?lang=fr#generating-csr" text="Générer une demande de signature de certificat (CSR)"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html?lang=fr#installing-ssl-certificate" text="Installation dʼun certificat SSL"

>[!IMPORTANT]
>
>Le renouvellement des certificats SSL depuis le panneau de contrôle est disponible en version bêta, et est sujet à de fréquentes mises à jour et modifications sans préavis.
>
>Si vous utilisez une instance avec un modèle d’hébergement hybride, vous ne pouvez afficher que les certificats associés aux sous-domaines délégués et ne pourrez pas les renouveler.

La procédure de renouvellement des certificats SSL comprend 3 étapes :

1. **Génération de la demande de signature de certificat (CSR)**

   La demande de signature de certificat doit être générée pour l’instance et les sous-domaines que vous envisagez de sécuriser avant d’acheter un certificat.  Vous devrez fournir certaines informations nécessaires à la génération de la demande de signature de certificat (telles que le nom commun, le nom et l’adresse de l’organisation, etc.). [En savoir plus](generate-csr.md)

1. **Achat du certificat SSL**

   Une fois la demande de signature de certificat générée, vous pouvez l’utiliser pour acheter le certificat SSL auprès de l’autorité de certification approuvée par votre société.

1. **Installation du certificat SSL**

   Installez le certificat SSL acheté sur le sous-domaine souhaité pour le sécuriser. [En savoir plus](install-ssl-certificate.md)

![](assets/do-not-localize/how-to-video.png) Découvrez cette fonctionnalité en vidéo dans [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=fr#subdomains-and-certificates) ou [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=fr#adding-ssl-certificates).

**Rubriques connexes :**

* [Guide des bonnes pratiques en matière de délivrabilité - Processus de demande de certificat SSL pour Adobe Campaign](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/campaign/ac-ssl-certificate-request.html)
* [Marque des sous-domaines](../../subdomains-certificates/using/subdomains-branding.md)
* [Surveillance de vos sous-domaines](../../subdomains-certificates/using/monitoring-subdomains.md)
