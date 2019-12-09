---
title: Gestion des certificats SSL des sous-domaines
description: Découvrez comment surveiller les certificats SSL de vos sous-domaines et lancer leur processus de renouvellement
translation-type: tm+mt
source-git-commit: 6bc165f995d34d21b5bce379db3095317db10906

---


# Gestion des certificats SSL des sous-domaines {#managing-subdomains-ssl-certificates}

La carte **[!UICONTROL Sous-domaines et Certificats]**vous permet de déterminer ceux de vos sous-domaines et sous-domaines associés qui hébergent vos pages d’entrée et vos ressources avec des certificats SSL installés dessus. Vous pouvez également identifier facilement les sous-domaines comportant des certificats expirant afin de pouvoir anticiper leur expiration.

Si un certificat est sur le point d’expirer, vous pouvez alors lancer une demande d’assistance clientèle avec toutes les informations requises pour renouveler le certificat et assurer le bon fonctionnement de votre instance.

>[!NOTE]
>
>Adobe recommande de renouveler un certificat SSL des sous-domaines associés **lorsqu’il se rapproche de la date d’expiration**. Le renouvellement du certificat peut prendre quelques jours selon votre organisation. Nous vous recommandons d’allouer le temps approprié pour ce processus.

## Surveillance des certificats SSL {#monitoring-ssl-certificates}

La liste des sous-domaines de chaque instance est directement accessible lors de la sélection de la carte **[!UICONTROL Sous-domaines et certificats]**.

Les sous-domaines sont organisés selon la date d’expiration la plus proche du certificat SSL, avec des informations visuelles sur l’expiration, en jours :

* **Vert**: le sous-domaine n’a pas de certificat expirant dans les 60 jours suivants.
* **Orange**: un ou plusieurs sous-domaines possèdent un certificat qui expirera dans les 60 jours suivants.
* **Rouge**: un ou plusieurs sous-domaines disposent d’un certificat qui expirera dans les 30 prochains jours.

![](assets/visual_alert2.png)

Pour plus d’informations sur les certificats d’un sous-domaine, cliquez sur le bouton **[!UICONTROL Détails du certificat]**.

![](assets/certificate_details4.png)

La liste de tous les sous-domaines connexes s’affichera sur leurs certificats. Elle comprend généralement des sous-domaines de pages d&#39;entrée, de pages de ressources, etc.

![](assets/monitoring_subdomains_details2.png)

Si nécessaire, vous pouvez lancer une demande de renouvellement de certificat à partir de cette fenêtre. Pour plus d&#39;informations, reportez-vous à la section ci-dessous.

## Lancement du renouvellement des certificats SSL {#initiating-ssl-certificate-renewal}

>[!NOTE]
>
>Le Panneau de configuration ne gère pas automatiquement le renouvellement du certificat. Il vous permet uniquement de **lancer le processus** de renouvellement en préparant la demande à envoyer au service à la clientèle d’Adobe Campaign.

Le processus de renouvellement du certificat SSL comprend 3 étapes :

1. **Génération de la demande de signature de certificat (CSR) Le service à la clientèle** Adobe génère une demande de signature de certificat pour vous, sur la demande effectuée via le portail du service à la clientèle. Vous devrez fournir certaines informations nécessaires à la génération de la demande de service client (nom commun, nom et adresse de l’organisation, etc.). Dans le Panneau de configuration, vous pouvez afficher la liste des éléments requis lors du lancement du processus de renouvellement. Pour plus d&#39;informations, reportez-vous à la section ci-dessous.
1. **Achat du certificat** SSL Une fois que le service d’assistance clientèle a généré le CSR, vous pouvez le télécharger et acheter le certificat SSL auprès de l’autorité de certification approuvée par votre entreprise.
1. **Installation du certificat** SSL Une fois le certificat SSL acheté, vous devez le fournir au service à la clientèle Adobe. Le certificat sera installé et vous verrez les dates d’expiration mises à jour des certificats dans le Panneau de configuration.

Pour lancer le renouvellement des certificats SSL dans le Panneau de configuration, procédez comme suit :

1. Ouvrez la carte **[!UICONTROL Sous-domaines et certificats]**, puis cliquez sur l’icône**[!UICONTROL  Détails du certificat]** du sous-domaine avec les certificats arrivant à expiration.

   ![](assets/renewal1.png)

1. La liste des sous-domaines associés s’affiche. Elle comprend généralement des sous-domaines de landing pages, de pages de ressources, etc.
Cliquez sur le bouton **[!UICONTROL Détails du ticket]**pour lancer le processus de renouvellement des certificats.

   ![](assets/renewal2.png)

1. Un formulaire s’affiche, avec tous les détails requis pour renouveler votre certificat SSL. Veillez à renseigner les informations demandées de manière complète et précise (si nécessaire, contactez votre équipe interne, votre équipe de sécurité et votre équipe informatique). Sinon, une demande de signature de certificat ne peut pas être générée et vous ne pourrez pas renouveler le certificat.

   * **[!UICONTROL Organisation]**IMS : ID de votre organisation.
   * **[!UICONTROL Instance]**: URL de l’instance Campaign associée au sous-domaine.
   * **[!UICONTROL Nom]**commun : Il s’agit généralement d’une URL de sous-domaine de suivi, associée au sous-domaine avec le certificat expirant.
   * **[!UICONTROL Sous-domaines]**: Sous-domaines liés au sous-domaine avec un certificat expirant. Si vous souhaitez appliquer un certificat SSL unique à d’autres sous-domaines, vous pouvez les ajouter à cette liste. Dans ce cas, assurez-vous que ces sous-domaines sont associés à la même organisation IMS et à la même URL d’instance.
   >[!CAUTION]
   >
   >The **[!UICONTROL IMS Org]**and**[!UICONTROL  Instance]** fields are filled in automatically by the Control Panel and should not be modified.

   ![](assets/renewal3.png)

1. Une fois le formulaire rempli, cliquez sur le bouton **[!UICONTROL Copier les détails]**pour enregistrer les informations dans le Presse-papiers.

   >[!NOTE]
   >
   >Si vous n’effacez pas l’historique de votre navigateur, les informations que vous avez saisies seront enregistrées, ce qui vous permettra de les utiliser pour renouveler le certificat ultérieurement.

1. Cliquez sur le bouton **[!UICONTROL Enregistrer le nouveau ticket]**. Vous êtes automatiquement redirigé vers la page de connexion du service à la clientèle d’Adobe Campaign.

   ![](assets/renewal4.png)

1. Connectez-vous, puis créez un ticket d’assistance avec l’objet &quot;Requête CSR de certificat SSL&quot;.
Collez toutes les informations copiées précédemment dans le corps du ticket, puis cliquez sur Envoyer.

   >[!NOTE]
   >
   >Si vous n’avez pas les privilèges nécessaires pour déposer des dossiers d’assistance pour votre entreprise, veuillez transmettre toutes les informations que vous avez copiées dans le Presse-papiers à votre contact d’assistance et leur demander d’ouvrir un nouveau ticket d’assistance clientèle pour vous.

**Rubriques connexes :**

* [Didacticiel vidéo sur Campaign Standard](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/managing-ssl-certificates.html)
* [Didacticiel vidéo sur Campaign Classic](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/managing-ssl-certificates.html)
