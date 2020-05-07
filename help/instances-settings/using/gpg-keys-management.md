---
title: Gestion des clés GPG
description: Découvrez comment gérer les clés GPG pour chiffrer et déchiffrer les données dans Adobe Campaign.
translation-type: tm+mt
source-git-commit: d44c0557904f0e6f6688c12687fbf84e42553d6b
workflow-type: tm+mt
source-wordcount: '1051'
ht-degree: 3%

---


# Gestion des clés GPG {#gpg-keys-management}

## A propos du chiffrement GPG {#about-gpg-encryption}

Le cryptage GPG vous permet de protéger vos données à l&#39;aide d&#39;un système de paires clés public-privé qui respecte la spécification [OpenPGP](https://www.openpgp.org/about/standard/) .

Une fois implémentées, les données entrantes peuvent être déchiffrées et les données sortantes chiffrées avant le transfert, afin de vous assurer qu’elles ne seront accessibles à personne sans une paire de clés correspondante valide.

Pour mettre en oeuvre le chiffrement GPG avec Campaign, les clés GPG doivent être installées et/ou générées sur une instance marketing par un utilisateur administrateur directement à partir du Panneau de configuration.

Vous pourrez alors :

* **Chiffrer les données** envoyées : Adobe Campaign envoie les données après les avoir chiffrées avec la clé publique installée.

* **Décrypter les données** entrantes : Adobe Campaign reçoit des données chiffrées à partir d’un système externe à l’aide d’une clé publique téléchargée à partir du Panneau de configuration. Adobe Campaign décrypte les données à l’aide d’une clé privée générée à partir du Panneau de configuration.

## Surveillance des clés GPG

Pour accéder aux clés GPG installées et générées pour vos instances, ouvrez la carte des paramètres **[!UICONTROL de l&#39;]** instance, puis sélectionnez l&#39;onglet **[!UICONTROL GPG keys]** .

![](assets/gpg_list.png)

La liste affiche toutes les clés GPG de chiffrement et de déchiffrement qui ont été installées et générées pour vos instances avec des informations détaillées sur chaque clé :

* **[!UICONTROL Nom]**: Nom défini lors de l’installation ou de la génération de la clé.
* **[!UICONTROL Cas]** d’utilisation : Cette colonne spécifie la casse d’utilisation de la clé :

   ![](assets/gpg_icon_encrypt.png): La clé a été installée pour le chiffrement des données.

   ![](assets/gpg_icon_decrypt.png): La clé a été générée pour permettre le déchiffrement des données.

* **[!UICONTROL Empreinte digitale]**: l&#39;empreinte de la clé.
* **[!UICONTROL Expires]**: Date d&#39;expiration de la clé. Notez que le Panneau de configuration fournira des indications visuelles à l&#39;approche de sa date d&#39;expiration :

   * Urgent (rouge) s’affiche 30 jours avant.
   * L’avertissement (jaune) s’affiche 60 jours auparavant.
   * Une bannière rouge &quot;Expiré&quot; s’affiche une fois qu’une clé arrive à expiration.
   >[!NOTE]
   >
   >Notez qu’aucune notification par courrier électronique ne sera envoyée par le Panneau de configuration.

Il est recommandé de supprimer toute clé dont vous n’avez plus besoin. Pour ce faire, cliquez sur le bouton **..** , puis sélectionnez **[!UICONTROL Supprimer la clé].**.

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>Avant de supprimer une clé, assurez-vous qu’elle n’est utilisée dans aucun processus Adobe Campaign pour éviter qu’elle ne s’effondre.

## Chiffrement des données {#encrypting-data}

Le Panneau de configuration vous permet de chiffrer les données provenant de votre instance Adobe Campaign.

Pour ce faire, vous devez générer une paire de clés GPG à partir d&#39;un outil de chiffrement PGP, puis installer la clé publique dans le Panneau de configuration. Vous pourrez alors chiffrer les données avant de les envoyer à partir de votre instance. Pour ce faire, procédez comme suit :

1. Générez une paire de clés publique/privée à l&#39;aide d&#39;un outil de chiffrement GPG après la spécification [](https://www.openpgp.org/about/standard/)OpenPGP. Pour ce faire, installez un utilitaire GPG ou un logiciel GNuPG.

   >[!NOTE]
   >
   >Un logiciel libre pour générer des clés est disponible. Toutefois, veillez à respecter les directives de votre entreprise et à utiliser l’utilitaire PGP recommandé par votre entreprise informatique/sécurité.

1. Une fois l&#39;utilitaire installé, exécutez la commande ci-dessous, dans Mac Terminal ou Windows Machine.

   `gpg --full-generate-key`

1. Lorsque vous y êtes invité, spécifiez les paramètres de votre clé. Les paramètres requis sont les suivants :

   * **type** de clé : RSA
   * **longueur** de clé : 1 024 à 4 096 bits
   * **nom** réel et adresse ****&#x200B;électronique : Permet de suivre qui a créé la paire de clés. Entrez un nom et une adresse électronique liés à votre organisation ou votre service.
   * **commentaire**: l’ajout d’une étiquette au champ de commentaire vous permet d’identifier facilement la clé dans la liste des clés du Panneau de configuration.
   * **expiration**: Date ou &quot;0&quot; sans date d’expiration.
   * **phrase secrète**
   ![](assets/gpg_command.png)

1. Une fois confirmé, le script génère une clé que vous pouvez exporter dans un fichier ou coller directement dans le Panneau de configuration. Pour exporter le fichier, exécutez cette commande suivie de l&#39;empreinte de la clé que vous avez générée.

   `gpg -a --export <fingerprint>`

1. Pour installer la clé publique dans le Panneau de configuration, accédez à l&#39;onglet Clés **** GPG, puis sélectionnez l&#39;instance de votre choix.

1. Cliquez sur le bouton **[!UICONTROL Installer la clé]** .

   ![](assets/gpg_install_button.png)

1. Collez la clé publique qui a été générée à partir de votre outil de chiffrement PGP. Vous pouvez également faire glisser directement le fichier de clé publique.

   >[!NOTE]
   >
   >La clé publique doit être au format OpenPGP.

   ![](assets/gpg_install_paste.png)

1. Cliquez sur le bouton **!UICONTROL Installer la clé]**.

Une fois la clé publique installée, elle s’affiche dans la liste. Vous pouvez utiliser le **...** bouton pour le télécharger ou copier son empreinte digitale.

![](assets/gpg_install_download.png)

La clé est ensuite disponible pour utilisation dans les workflows Adobe Campaign. Vous pouvez l’utiliser pour chiffrer des données lors de l’utilisation d’activités d’extraction de données.

Pour plus d&#39;informations à ce sujet, reportez-vous à la documentation Adobe Campaign :

| Campaign Classic | Campaign Standard |
---------|----------
| [Compresser ou chiffrer un fichier](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#zipping-or-encrypting-a-file) | [Gérer des données cryptées](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/importing-data.html#managing-encrypted-data) |
| [activité d’extraction de données (fichier)](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/action-activities/extraction--file-.html) | [Activité Extraction de fichier](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/data-management-activities/extract-file.html) |

## Décryptage des données {#decrypting-data}

Le Panneau de configuration vous permet de déchiffrer des données externes provenant de vos instances Adobe Campaign.

Pour ce faire, vous devez générer une paire de clés GPG directement à partir du Panneau de configuration.

* La clé **** publique sera partagée avec le système externe, qui l&#39;utilisera pour chiffrer les données à envoyer à Campaign.
* Campaign utilisera la clé **** privée pour déchiffrer les données chiffrées entrantes.

Pour générer une paire de clés dans le Panneau de configuration, procédez comme suit :

1. Accédez à l&#39;onglet Clés **** GPG, puis sélectionnez l&#39;instance Adobe Campaign de votre choix.

1. Cliquez sur le bouton **[!UICONTROL Générer une clé]** .

   ![](assets/gpg_generate.png)

1. Indiquez le nom de la clé, puis cliquez sur **!UICONTROL Générer la clé]**. Ce nom vous aidera à identifier la clé à utiliser pour le déchiffrement dans les Workflows de campagne

   ![](assets/gpg_generate_name.png)

Une fois la paire de clés générée, la clé publique s’affiche dans la liste. Notez que les paires de clés de déchiffrement sont générées sans date d’expiration.

Vous pouvez utiliser le **...** bouton pour télécharger la clé publique ou copier son empreinte digitale.

![](assets/gpg_generate_list.png)

La clé publique est alors disponible pour être partagée avec tout système externe. Adobe Campaign pourra utiliser la clé privée dans les activités de chargement de données pour déchiffrer les données chiffrées à l’aide de la clé publique.

Pour plus d&#39;informations à ce sujet, reportez-vous à la documentation Adobe Campaign :

| Campaign Classic | Campaign Standard |
---------|----------
| [Décompresser ou déchiffrer un fichier avant traitement](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/importing-data.html#unzipping-or-decrypting-a-file-before-processing) | [Gérer des données cryptées](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/importing-data.html#managing-encrypted-data) |
| [activité de chargement de données (fichier)](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/action-activities/data-loading--file-.html) | [Activité Chargement de fichier](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/data-management-activities/load-file.html) |
