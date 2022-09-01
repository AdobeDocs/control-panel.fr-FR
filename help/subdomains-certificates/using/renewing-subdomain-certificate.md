---
product: campaign
solution: Campaign
title: Renouvellement du certificat SSL d’un sous-domaine
description: Découvrez comment renouveler les certificats SSL de vos sous-domaines
feature: Control Panel
role: Architect
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: 963c2af5cdca80ebc2cd79e0708dc4dfe8c6ec1e
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# Renouvellement dʼun certificat SSL {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="Renouvellement du certificat SSL"
>abstract="Pour renouveler un certificat SSL, vous devez générer une demande de signature de certificat (CSR), acheter le certificat SSL pour vos sous-domaines et installer l’ensemble de certificats."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html?lang=fr#generating-csr" text="Générer une demande de signature de certificat (CSR)"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html?lang=fr#installing-ssl-certificate" text="Installation dʼun certificat SSL"

La procédure de renouvellement des certificats SSL comprend 3 étapes :

1. **Génération de la demande de signature de certificat (CSR)**

   La demande de signature de certificat doit être générée pour l’instance et les sous-domaines que vous envisagez de sécuriser avant d’acheter un certificat.  Vous devrez fournir certaines informations nécessaires à la génération de la demande de signature de certificat (telles que le nom commun, le nom et l’adresse de l’organisation, etc.). [En savoir plus](generate-csr.md)

1. **Achat du certificat SSL**

   Une fois la CSR générée, vous pouvez l’utiliser pour acheter le certificat SSL auprès de l’autorité de certification approuvée par votre entreprise.

1. **Installation du certificat SSL**

   Installez le certificat SSL acheté sur le sous-domaine souhaité pour le sécuriser. [En savoir plus](install-ssl-certificate.md)

![](assets/do-not-localize/how-to-video.png) Découvrez cette fonctionnalité en vidéo dans [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=fr#subdomains-and-certificates) ou [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=fr#adding-ssl-certificates).

**Rubriques connexes :**

* [Guide des bonnes pratiques en matière de délivrabilité - Processus de demande de certificat SSL pour Adobe Campaign](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/campaign/ac-ssl-certificate-request.html?lang=fr)
* [Marque des sous-domaines](../../subdomains-certificates/using/subdomains-branding.md)
* [Surveillance de vos sous-domaines](../../subdomains-certificates/using/monitoring-subdomains.md)
