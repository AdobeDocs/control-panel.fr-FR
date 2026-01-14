---
product: campaign
solution: Campaign
title: Ajouter des enregistrements de vérification de site Google pour un sous-domaine
description: Découvrez comment ajouter un enregistrement de vérification de site Google pour un sous-domaine afin de vérifier la propriété du domaine.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: 547ca6f2-720f-4d58-b31b-5b2611ba9156
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '280'
ht-degree: 100%

---

# Ajouter des enregistrements de vérification de site Google {#adding-a-google-txt-record}

Pour garantir des taux de réception d’emails élevés et des taux de spam bas, certains services comme Google exigent que vous ajoutiez un enregistrement TXT aux paramètres de votre domaine pour vérifier que vous en êtes propriétaire.

Actuellement, Gmail est l’un des fournisseurs d’adresses e-mail les plus utilisés. Pour garantir une bonne délivrabilité et une diffusion réussie des emails vers les adresses Gmail, Adobe Campaign permet d’ajouter des enregistrements TXT de vérification de site Google spéciaux à vos sous-domaines afin de s’assurer qu&#39;ils soient vérifiés.

Pour ajouter un enregistrement TXT Google à un sous-domaine utilisé pour envoyer des e-mails à des adresses Gmail, procédez comme suit :

1. Dans la liste des sous-domaines, cliquez sur le bouton représentant des points de suspension en regard du sous-domaine souhaité, puis sélectionnez **[!UICONTROL Détails du sous-domaine]**.

1. Cliquez sur le bouton **[!UICONTROL Ajouter un enregistrement TXT]**, puis choisissez **[!UICONTROL Vérification de site Google]** dans la liste déroulante **[!UICONTROL Type d’enregistrement]**.

1. Saisissez la valeur générée dans les outils G Suite Admin. Pour plus d’informations, consultez [l’aide de G Suite Admin](https://support.google.com/a/answer/183895).

   ![](assets/txt_addtxt.png)

1. Cliquez sur le bouton **[!UICONTROL Ajouter]** pour confirmer l’opération.

   ![](assets/txt_txtadded.png)

Une fois l’enregistrement TXT ajouté, vous devez le faire vérifier par Google. Pour cela, accédez aux outils G Suite Admin, puis lancez l’étape de vérification (voir [l’aide de G Suite Admin](https://support.google.com/a/answer/183895)).

Pour supprimer un enregistrement, sélectionnez-le dans la liste des enregistrements, puis cliquez sur le bouton Supprimer.

>[!NOTE]
>
>Le seul enregistrement que vous pouvez supprimer de la liste des enregistrements DNS est celui qui vient d’être ajouté (dans notre cas, l’enregistrement Google TXT).

![](assets/do-not-localize/how-to-video.png) Découvrez cette fonctionnalité en vidéo dans [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html?lang=fr#subdomains-and-certificates) ou [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html?lang=fr#subdomains-and-certificates).
