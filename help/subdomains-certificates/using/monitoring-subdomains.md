---
product: campaign
solution: Campaign
title: Surveiller vos sous-domaines
description: Surveillez vos sous-domaines pour vous assurer qu’ils sont tous correctement configurés pour fonctionner avec Adobe Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: 76c42ba45b3430b1b93458f18b1b0e78f289fad1
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 72%

---

# Surveiller vos sous-domaines {#monitoring-subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Suppression des sous-domaines délégués "
>abstract="Cet écran vous permet de supprimer tout sous-domaine qui a été délégué dans Panneau de Contrôle. Gardez à l’esprit que la suppression d’un sous-domaine ne peut pas être annulée et sera irréversible une fois effectuée.<br><br>Si vous essayez de supprimer le domaine Principal de l’instance sélectionnée, vous serez invité à choisir le domaine qui le remplacera."

Il est essentiel de surveiller vos sous-domaines pour vous assurer qu’ils sont tous correctement configurés pour fonctionner avec Adobe Campaign.

La liste des sous-domaines de chacune de vos instances de production est directement accessible en sélectionnant la carte **[!UICONTROL Sous-domaines et certificats]**.

La colonne **[!UICONTROL Dernière vérification]** indique à quel moment un sous-domaine a été vérifié pour la dernière fois. Vous pouvez lancer une vérification à tout moment en cliquant sur le bouton **...** / **[!UICONTROL Vérifier le sous-domaine]**.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe déconseille d’utiliser des sous-domaines sans date de certificat, car cela peut entraîner des problèmes de délivrabilité pour ceux-ci.

Lors du lancement d’une vérification, plusieurs opérations sont effectuées pour contrôler que le sous-domaine est correctement configuré (contrôle du tenant d’instance, test d’envoi d’email, etc.)

Si la vérification du sous-domaine échoue, contactez l’assistance clientèle Adobe pour plus d’informations.

**Rubriques connexes :**

* [Renouvellement du certificat SSL d’un sous-domaine](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Marque des sous-domaines](../../subdomains-certificates/using/subdomains-branding.md)
