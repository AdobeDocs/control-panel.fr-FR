---
product: campaign
solution: Campaign
title: Gestion des enregistrements TXT
description: Découvrez comment gérer les enregistrements TXT pour vérifier le propriétaire du domaine.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 118fa4d722980e507d15647453e96a8b6189f837
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 25%

---


# Prise en main des enregistrements TXT {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="Gestion des enregistrements TXT"
>abstract="Les enregistrements TXT font partie des enregistrements DNS. Ils servent à donner des informations textuelles à propos d’un domaine, que des sources externes pourront lire par la suite. Panneau de Contrôle vous permet d’ajouter trois types d’enregistrements à vos sous-domaines : les enregistrements Google Site Verification, DMARC et BIMI."

## À propos des enregistrements TXT {#about}

Les enregistrements TXT font partie des enregistrements DNS. Ils servent à donner des informations textuelles à propos d’un domaine, que des sources externes pourront lire par la suite. Panneau de Contrôle vous permet d’ajouter trois types d’enregistrements à vos sous-domaines :

* **Enregistrements TXT Google** vous permettent d’attester que vous êtes propriétaire de votre domaine, en veillant à des taux de boîte de réception élevés et à des taux de spam bas pour vos emails. [Découvrez comment ajouter des enregistrements TXT Google](managing-txt-records.md)
* **Enregistrements DMARC** fournir un moyen d’authentifier le domaine de l’expéditeur et d’empêcher l’utilisation non autorisée du domaine à des fins malveillantes. [Découvrez comment ajouter des enregistrements DMARC](dmarc.md)
* **Enregistrements BIMI** vous permettent d’afficher un logo approuvé en regard de vos emails dans les boîtes de réception des fournisseurs de messagerie afin d’améliorer la reconnaissance et la confiance de la marque. [Découvrez comment ajouter des enregistrements BIMI](bimi.md)

## Surveillance des enregistrements de vos sous-domaines {#monitor}

Vous pouvez surveiller tous les enregistrements TXT ajoutés pour chaque sous-domaine en accédant aux détails des sous-domaines.

Dans cet écran, tous les enregistrements de type TXT pour le sous-domaine sélectionné s’affichent avec les informations de la colonne &quot;Valeur&quot; sur leur configuration. Pour supprimer un enregistrement Google TXT, DMARC ou BIMI, cliquez sur le bouton représentant des points de suspension, puis sélectionnez Supprimer. Vous pouvez également modifier les enregistrements DMARC et BIMI si nécessaire.

![](assets/txt-records.png)
