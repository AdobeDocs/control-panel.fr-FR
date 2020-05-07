---
title: Gestion des enregistrements TXT
description: Découvrez comment gérer les enregistrements TXT pour vérifier le propriétaire du domaine.
translation-type: tm+mt
source-git-commit: 7c2dd60c70b5f9c0b2567df289582b972a7f76b8
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 100%

---


# Gestion des enregistrements TXT {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="Gestion des enregistrements TXT"
>abstract="Certains services comme Google exigent que vous ajoutiez un enregistrement TXT aux paramètres de votre domaine pour vérifier que vous en êtes propriétaire."

## À propos des enregistrements TXT {#about-txt-records}

Les enregistrements TXT font partie des enregistrements DNS. Ils servent à donner des informations textuelles à propos d’un domaine, que des sources externes pourront lire par la suite.

Pour garantir des taux de réception d’emails élevés et des taux de spam bas, certains services comme Google exigent que vous ajoutiez un enregistrement TXT aux paramètres de votre domaine pour vérifier que vous en êtes propriétaire.

Actuellement, Gmail est l’un des fournisseurs d’adresses email les plus utilisés. Pour garantir une bonne délivrabilité et une diffusion réussie des emails vers les adresses Gmail, Adobe Campaign permet d’ajouter des enregistrements TXT de vérification de site Google spéciaux à vos sous-domaines afin de s’assurer qu&#39;ils soient vérifiés.

Ressources supplémentaires :

* [Tutoriel vidéo sur Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/administrating/control-panel/google-txt-record-management.html)
* [Tutoriel vidéo sur Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic-learn/tutorials/administrating/control-panel-acc/google-txt-record-management.html)

## Ajout d’un enregistrement TXT Google pour un sous-domaine {#adding-a-google-txt-record}

Pour ajouter un enregistrement TXT Google à un sous-domaine utilisé pour envoyer des emails à des adresses Gmail, procédez comme suit :

1. Accédez à la carte **[!UICONTROL Sous-domaines et certificats]**.

1. Sélectionnez votre instance, puis ouvrez les détails du sous-domaine auquel vous souhaitez ajouter un enregistrement DNS.

   ![](assets/txt_subdomaindetails.png)

1. Cliquez sur le bouton **[!UICONTROL Ajouter un enregistrement TXT]**, puis saisissez la valeur générée dans les outils G Suite Admin. Pour plus d’informations, voir [l’aide de G Suite Admin](https://support.google.com/a/answer/183895).

   ![](assets/txt_addtxt.png)

1. Cliquez sur le bouton **[!UICONTROL Ajouter]** pour confirmer l’opération.

   ![](assets/txt_txtadded.png)

Une fois l’enregistrement TXT ajouté, vous devez le faire vérifier par Google. Pour cela, accédez aux outils G Suite Admin, puis lancez l’étape de vérification (voir [l’aide de G Suite Admin](https://support.google.com/a/answer/183895)).

Pour supprimer un enregistrement, sélectionnez-le dans la liste des enregistrements, puis cliquez sur le bouton Supprimer.

>[!NOTE]
>
>Le seul enregistrement que vous pouvez supprimer de la liste des enregistrements DNS est celui qui vient d’être ajouté (dans notre cas, l’enregistrement Google TXT).
