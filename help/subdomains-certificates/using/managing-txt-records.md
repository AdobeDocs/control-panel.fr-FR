---
title: Gestion des enregistrements TXT
description: Découvrez comment gérer les enregistrements TXT pour la vérification de la propriété de domaine.
translation-type: tm+mt
source-git-commit: 3ce9f62be9df0f6e6a61c16ddaf3ab8ae58712ce

---


# Gestion des enregistrements TXT {#managing-txt-records}

>[!CONTEXTUALHELP]
>id=&quot;cp_siteverification_add&quot;
>title=&quot;Gestion des enregistrements TXT&quot;
>abstract=&quot;Certains services comme Google exigent que vous ajoutiez un enregistrement TXT aux paramètres de votre domaine afin de vérifier que vous êtes propriétaire du domaine.&quot;

## A propos des enregistrements TXT {#about-txt-records}

Les enregistrements TXT sont un type d’enregistrements DNS utilisés pour fournir des informations textuelles sur un domaine, qui peuvent être lues par des sources externes.

Afin d’assurer des taux de boîte de réception élevés et des taux de spam bas, certains services comme Google exigent que vous ajoutiez un enregistrement TXT aux paramètres de votre domaine afin de vérifier que vous êtes propriétaire du domaine.

Actuellement, Gmail est l&#39;un des fournisseurs d&#39;adresses électroniques les plus populaires. Afin d&#39;assurer une bonne délivrabilité et un réussi des courriels aux adresses Gmail,  vous permet d&#39;ajouter des enregistrements TXT spéciaux de vérification de site Google à vos sous-domaines pour vous assurer qu&#39;ils sont vérifiés.

## Ajout d’un enregistrement Google TXT pour un sous-domaine {#adding-a-google-txt-record}

Pour ajouter un enregistrement Google TXT à votre sous-domaine utilisé pour envoyer des adresses Gmail, procédez comme suit :

1. Accédez à la **[!UICONTROL Subdomain and Certificates]** carte.

1. Sélectionnez votre instance, puis ouvrez les détails du sous-domaine auquel vous souhaitez ajouter un enregistrement DNS.

   ![](assets/txt_subdomaindetails.png)

1. Cliquez sur le **[!UICONTROL Add TXT record]** bouton, puis entrez la valeur générée dans les outils d’administration de la Suite G. Pour plus d’informations, reportez-vous à l’Aide [de l’administrateur de la Suite](https://support.google.com/a/answer/183895)G.

   ![](assets/txt_addtxt.png)

1. Cliquez sur le **[!UICONTROL Add]** bouton pour confirmer.

   ![](assets/txt_txtadded.png)

Une fois l’enregistrement TXT ajouté, vous devez le faire vérifier par Google. Pour ce faire, accédez aux outils d’administration de la Suite G, puis lancez l’étape de vérification (voir Aide [de l’administrateur de la Suite](https://support.google.com/a/answer/183895)G).


Pour supprimer un enregistrement, sélectionnez-le dans le d&#39;enregistrements, puis cliquez sur le bouton Supprimer.

>[!NOTE]
>
>Le seul enregistrement que vous pouvez supprimer du d&#39;enregistrements DNS est celui que vous avez précédemment ajouté (dans notre cas, l&#39;enregistrement Google TXT).
