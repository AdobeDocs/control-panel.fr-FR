---
title: Documentation du produit
description: Documentation du Panneau de contrôle.
feature: Control Panel
role: Admin
level: Experienced
exl-id: 2b2cfaed-e42e-4c3a-a8d8-224b936890ab
source-git-commit: e8bffd8e7f571fd85c725adf837c2997f7615fcd
workflow-type: ht
source-wordcount: '290'
ht-degree: 100%

---

# Centre dʼaide {#control-panel-documentation}

>[!CONTEXTUALHELP]
>id="cp_overview"
>title="À propos du Panneau de contrôle"
>abstract="La page d’accueil du Panneau de contrôle vous donne accès à toutes les actions qui peuvent être effectuées sur vos instances Campaign."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/accessing-control-panel.html?lang=fr" text="Accès au Panneau de contrôle"

Le Panneau de contrôle de Campaign accroît votre efficacité en tant quʼadministrateur de produit Campaign Standard et v7/v8, en vous permettant de gérer les paramètres et de suivre lʼutilisation de chacune de vos instances Campaign.

## Nouveautés

**Interface utilisateur**

* Le panneau de contrôle est désormais disponible dans d’autres langues. [En savoir plus](discover/using/discovering-the-interface.md#supported-languages-languages)

**Surveillance des profils actifs**

* Vous pouvez désormais surveiller le nombre de profils actifs auxquels vous avez droit et le nombre total de profils utilisés dans votre organisation dans toutes les instances, si vous utilisez plusieurs instances. [En savoir plus](performance-monitoring/using/active-profiles-monitoring.md)

**Enregistrements DMARC**

* Plusieurs adresses e-mail peuvent désormais recevoir des e-mails de rapport agrégé et de rapport d’échec. [En savoir plus](subdomains-certificates/using/dmarc.md)
* Des modifications ont été apportées si des enregistrements DMARC et BIMI existent pour un sous-domaine :

   * Les enregistrements DMARC ne peuvent pas être supprimés. Si vous souhaitez en supprimer un, vous devez d’abord supprimer l’enregistrement BIMI.
   * Les enregistrements DMARC peuvent être modifiés, mais la rétrogradation de la règle vers « Aucun » n’est pas autorisée et sa valeur en pourcentage doit être de 100.

>[!CAUTION]
>
>* Le Panneau de contrôle est accessible aux utilisateurs administrateurs uniquement. [Apprenez-en davantage](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=fr#discover-control-panel)
>
>* Pour Campaign v7, des restrictions de déploiement s’appliquent. [En savoir plus](faq.md#v7-restrictions)

## Ressources supplémentaires {#additional-resources}

<table>
    <tr>
        <td><b>Campaign Standard</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/control-panel-overview.html?lang=fr">Tutoriels vidéo sur le Panneau de contrôle</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-standard/using/campaign-standard-home.html?lang=fr">Documentation du produit Campaign Standard</a></li>
        </ul>
        </td>
        <td><b>Campaign v7</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/control-panel-overview.html?lang=fr">Tutoriels vidéo sur le Panneau de contrôle</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-classic/using/campaign-classic-home.html?lang=fr">Documentation du produit Campaign v7</a></li>
        </ul>
        </td>
        <td><b>Campaign v8</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-learn/control-panel/control-panel-overview.html?lang=fr">Tutoriels vidéo sur le Panneau de contrôle</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/campaign-home.html?lang=fr">Documentation du produit Campaign v8</a></li>
        </ul>
        </td>
    </tr>
</table>
