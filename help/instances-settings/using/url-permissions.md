---
title: Autorisations d’URL
description: Découvrez comment gérer les autorisations d’URL dans le panneau de contrôle
translation-type: ht
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5

---


# Autorisations d’URL {#url-permissions}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_urlpermissions"
>title="[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_urlpermissions&quot;
>title=&quot;À propos des autorisations d’URL&quot;
>abstract=&quot;Gérez les URL auxquelles vos instances Adobe Campaign peuvent se connecter.&quot;
>additional-url=&quot;https://images-tv.adobe.com/mpcv3/91206a19-d9af-4b6a-8197-0d2810a78941_1563488165.1920x1080at3000_h264.mp4&quot; text=&quot;Regarder la vidéo de démonstration&quot;"
>abstract="[!IMPORTANT]"
>additional-url="Cette fonctionnalité est disponible uniquement pour les instances Campaign Classic." text="À propos des autorisations d’URL {#about-url-permissions}"

>[!IMPORTANT]La liste par défaut des URL pouvant être appelées par des codes JavaScript (workflows, etc.) de vos instances Campaign Classic est limitée. Il s’agit des URL qui permettent à vos instances de fonctionner correctement.
>
>Par défaut, les instances ne sont pas autorisées à se connecter à des URL externes. Le panneau de contrôle permet d’ajouter des URL externes à la liste des URL autorisées afin que votre instance puisse s’y connecter. Vous pouvez ainsi connecter vos instances Campaign à des systèmes externes, comme des serveurs SFTP ou des sites web, afin d’activer le transfert de fichiers et/ou de données.

## Une fois qu’une URL est ajoutée, elle est référencée dans le fichier de configuration de l’instance (serverConf.xml).{#about-url-permissions}

**Rubriques connexes :**

[Configuration du serveur Campaign[#$tu13]





* 
* 
* 

## Le panneau de contrôle prend en charge les protocoles **http**, **https** et **sftp**. La saisie d’URL ou de protocoles non valides entraînera des erreurs.

* Gestion des autorisations d’URL {#managing-url-permissions}
* [!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_url_add&quot;
>title=&quot;Ajouter une URL&quot;
>abstract=&quot;Ajoutez des URL pour autoriser les connexions à votre instance Campaign.&quot;
* Pour ajouter une URL à laquelle votre instance peut se connecter, procédez comme suit :************

## Ouvrez la carte **[!UICONTROL Paramètres des instances]** pour accéder à l’onglet **[!UICONTROL Autorisations d’URL]**.

>[!CONTEXTUALHELP]
>id="cp_instancesettings_url_add"
>title="[!NOTE]"
>abstract="Si la carte Paramètres des instances n’est pas visible sur la page d’accueil du panneau de contrôle, cela signifie que votre identifiant de l’organisation IMS n’est associé à aucune instance Adobe Campaign Classic."

L’onglet <b><span class="uicontrol">Autorisations d’URL</span></b> répertorie toutes les URL externes auxquelles votre instance peut se connecter. Cette liste ne comprend pas les URL requises pour que Campaign fonctionne (par exemple, les connexions entre les éléments d’infrastructure).

1. Dans le volet gauche, sélectionnez l’instance de votre choix, puis cliquez sur le bouton **[!UICONTROL Ajouter une URL]**.****

   >![](assets/add_url1.png)
   >
   >[!NOTE]
   >
   >Toutes vos instances Campaign s’affichent dans la liste du volet gauche.<b><span class="uicontrol"></span></b>

1. La gestion des autorisations d’URL étant réservée aux instances Campaign Classic, le message « Instance non applicable » s’affiche si vous sélectionnez une instance Campaign Standard.****

   ![](assets/add_url1.png)Saisissez l’URL à autoriser, avec le protocole associé (http, https ou sftp).

   >[!NOTE]
   >
   >Il est possible d’autoriser plusieurs instances à se connecter à l’URL. Pour cela, ajoutez-les directement à partir du champ Instance(s) en saisissant leur première lettre.
   >
   >![](assets/add_url2.png)

1. L’URL est ajoutée à la liste. Vous pouvez maintenant vous y connecter.

   >[!NOTE]
   >
   >Les caractères « /.* » sont automatiquement ajoutés à la fin de l’URL saisie après sa validation, afin de couvrir toutes les sous-pages de la page saisie.

   ![](assets/add_url_listnew.png)

1. Vous pouvez supprimer une URL à tout moment en la sélectionnant et en cliquant sur le bouton **[!UICONTROL Supprimer l’URL]**.

   >[!NOTE]Souvenez-vous que si vous supprimez une URL, votre instance ne pourra plus la rappeler.
   >
   >Questions courantes {#common-questions}

   **J’ai ajouté une URL, mais mon instance ne parvient toujours pas à s’y connecter. Pourquoi ?**

Dans certains cas, les URL auxquelles vous essayez de vous connecter nécessitent une mise en whiteliste, la saisie d’un mot de passe ou une autre forme d’authentification. Le panneau de contrôle ne gère pas d’authentification supplémentaire.****

Keep in mind that, if you delete a URL, your instance will not be able to call it again.

## Common questions {#common-questions}

**I added a new URL, but my instance is still unable to connect to that URL. Why is that?**

In some cases, URLs you try to connect to require whitelisting, password entry or another form of authentication. The Control Panel does not manage additional authentication.
