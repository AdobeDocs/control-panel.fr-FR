---
title: Surveillance des certificats SSL des sous-domaines
description: Découvrez comment surveiller les certificats SSL de vos sous-domaines
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Monitoring subdomains&#39; SSL certificates {#monitoring-ssl-certificates}

Adobe Campaign vous recommande de sécuriser les sous-domaines hébergeant vos landing pages, en particulier ceux qui recueillent des informations sensibles sur vos clients.

Le **cryptage SSL (Secure Socket Layer)** garantit la sécurité des sous-domaines que vous avez délégués à Adobe. Lorsque votre client remplit un formulaire web ou visite une landing page hébergée par Adobe Campaign, les informations sont envoyées par défaut via un protocole non sécurisé (HTTP). Pour assurer une sécurité supplémentaire, sécurisez les informations envoyées avec un protocole HTTPS. Par exemple, l’adresse du sous-domaine « http://info.monsiteweb.com/ » deviendra « https://info.monsiteweb.com/ ».

**Les certificats SSL ne sont pas installés sur les sous-domaines délégués**. Ils sont installés sur les sous-domaines associés, principalement ceux qui hébergent des landing pages, des pages de ressources, etc.

**Les certificats SSL sont fournis pour une période spécifique** (1 an, 60 jours, etc.). Lorsqu’un certificat arrive à expiration, vous pouvez rencontrer des problèmes lors de l’accès aux landing pages ou de l’utilisation de ressources du sous-domaine. Pour éviter cela, le panneau de contrôle permet de surveiller les certificats SSL de vos sous-domaines et de lancer une procédure de renouvellement.

![](assets/no_certificate.png)

Si l’un des certificats SSL de votre sous-domaine est sur le point d’expirer, vous pouvez le renouveler directement à partir du Panneau de configuration. Pour plus d&#39;informations à ce sujet, reportez-vous à cette section : [Renouvellement du certificat](../../subdomains-certificates/using/renewing-subdomain-certificate.md)SSL d’un sous-domaine.
