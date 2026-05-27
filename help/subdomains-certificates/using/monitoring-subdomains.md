---
product: campaign
solution: Campaign
title: Surveiller vos sous-domaines
description: Surveillez vos sous-domaines pour vous assurer qu’ils sont tous correctement configurés pour fonctionner avec Adobe Campaign.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
TQID: https://experienceleague.adobe.com/49fMBOZ2iN7xs7PpnYRLDHpQO5eXMTvn-veAxpjeH7w
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 06babfad697fb874f2b77c5204e30580c55cd0d1
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 77%

---

# Surveiller les sous-domaines {#monitoring-subdomains}

Il est essentiel de surveiller vos sous-domaines pour vous assurer qu’ils sont tous correctement configurés pour fonctionner avec Adobe Campaign.

La liste des sous-domaines de chacune de vos instances de production est directement accessible en sélectionnant la carte **[!UICONTROL Sous-domaines et certificats]**.

La colonne **[!UICONTROL Dernière vérification]** indique à quel moment un sous-domaine a été vérifié pour la dernière fois. Vous pouvez lancer une vérification à tout moment en cliquant sur le bouton **...** / **[!UICONTROL Vérifier le sous-domaine]**.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe déconseille d’utiliser des sous-domaines sans date de certificat, car cela peut entraîner des problèmes de délivrabilité pour ceux-ci.

Lors du lancement d’une vérification, plusieurs opérations sont effectuées pour vérifier que le sous-domaine est correctement configuré (vérification du tenant d’instance, test d’envoi d’e-mail, etc.) Si la vérification du sous-domaine échoue, contactez l’assistance clientèle Adobe pour plus d’informations.

**Rubriques connexes :**

* [Renouvellement du certificat SSL d’un sous-domaine](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Marque des sous-domaines](../../subdomains-certificates/using/subdomains-branding.md)
