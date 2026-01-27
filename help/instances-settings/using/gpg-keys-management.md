---
product: campaign
solution: Campaign
title: Gestion des clés GPG
description: Découvrez comment gérer les clés GPG pour chiffrer et déchiffrer les données dans Adobe Campaign.
feature: Control Panel, Encryption
role: Admin
level: Experienced
exl-id: 366dd2ea-c6be-41a2-a4d6-4ffecb5f3d39
source-git-commit: de33a10a168358d0f38ca776fbcd88e0ccf63ce2
workflow-type: ht
source-wordcount: '1146'
ht-degree: 100%

---

# Gestion des clés GPG {#gpg-keys-management}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_gpg_management"
>title="À propos des clés GPG"
>abstract="Cet onglet vous permet dʼinstaller et/ou générer des clés GPG sur une instance marketing pour chiffrer les données envoyées depuis Campaign et déchiffrer les données entrantes."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=fr" text="À propos du suivi des performances"

## À propos du chiffrement GPG {#about-gpg-encryption}

Le chiffrement GPG permet de protéger vos données à l’aide d’un système de paires de clés publique-privée qui respectent la spécification [OpenPGP](https://www.openpgp.org/about/standard/).

Une fois ce système mis en œuvre, les données entrantes peuvent être déchiffrées et les données sortantes chiffrées avant le transfert, afin qu’elles ne soient accessibles à personne sans une paire de clés correspondante valide.

Pour mettre en œuvre le chiffrement GPG avec Campaign, les clés GPG doivent être installées et/ou générées sur une instance marketing par un utilisateur administrateur directement à partir du Panneau de contrôle.

Vous pourrez alors :

* **Chiffrer les données envoyées** : Adobe Campaign envoie les données après les avoir chiffrées avec la clé publique installée.

* **Déchiffrer les données entrantes** : Adobe Campaign reçoit des données chiffrées à partir d’un système externe à l’aide d’une clé publique téléchargée à partir du Panneau de contrôle. Adobe Campaign déchiffre les données à l’aide d’une clé privée générée à partir du Panneau de contrôle.

## Chiffrement des données {#encrypting-data}

Le Panneau de contrôle permet de chiffrer les données provenant de votre instance Adobe Campaign.

Pour cela, vous devez générer une paire de clés GPG à partir d’un outil de chiffrement PGP, puis installer la clé publique dans le Panneau de contrôle. Vous pourrez alors chiffrer les données avant de les envoyer depuis votre instance. Pour ce faire, suivez les étapes ci-après.

>[!NOTE]
>
>Vous pouvez installer jusqu’à 60 clés GPG dans le panneau de contrôle.

![](assets/do-not-localize/how-to-video.png)[ Découvrez cette fonctionnalité en vidéo](#video)

1. Générez une paire de clés publique/privée à l’aide d’un outil de chiffrement PGP suivant la [spécification OpenPGP](https://www.openpgp.org/about/standard/). Pour cela, installez un utilitaire GPG ou un logiciel GNuPG.

   >[!NOTE]
   >
   >Des logiciels open source gratuits permettant de générer des clés sont disponibles. Veillez toutefois à respecter les directives de votre entreprise et à utiliser l’utilitaire GPG recommandé par le service informatique/de sécurité.

1. Une fois l’utilitaire installé, exécutez la commande ci-dessous, dans la commande Mac Terminal ou Windows.

   `gpg --full-generate-key`

1. Lorsque vous y êtes invité, spécifiez les paramètres de votre clé. Les paramètres requis sont les suivants :

   * **type de clé** : RSA
   * **longueur de clé** : 3 072 à 4 096 bits
   * **nom réel** et **adresse email** : permet de suivre qui a créé la paire de clés. Entrez un nom et une adresse email associés à votre organisation ou votre service.
   * **commentaire** : l’ajout d’un libellé au champ de commentaire vous aidera à identifier facilement la clé à utiliser pour chiffrer vos données.
     >[!IMPORTANT]
     >
     >Assurez-vous que ce champ n’est pas vide et qu’un commentaire est renseigné.

   * **Expiration** : date ou « 0 » pour aucune date d’expiration.
   * **mot de passe**

   ![](assets/do-not-localize/gpg_command.png)

1. Une fois confirmé, le script génère une clé avec son empreinte associée que vous pouvez exporter dans un fichier ou coller directement dans le Panneau de contrôle. Pour exporter le fichier, exécutez cette commande suivie de l’empreinte de la clé que vous avez générée.

   `gpg -a --export <fingerprint>`

1. Pour installer la clé publique dans le Panneau de contrôle, ouvrez la carte **[!UICONTROL Paramètres des instances]**, puis sélectionnez l’onglet **[!UICONTROL Clés GPG]** et l’instance de votre choix.

1. Cliquez sur le bouton **[!UICONTROL Installer la clé]**.

   ![](assets/gpg_install_button.png)

1. Collez la clé publique qui a été générée à partir de votre outil de chiffrement PGP. Vous pouvez également effectuer directement un glisser-déposer du fichier de clé publique que vous avez exporté.

   >[!NOTE]
   >
   >La clé publique doit être au format OpenPGP.

   ![](assets/gpg_install_paste.png)

1. Cliquez sur le bouton **[!UICONTROL Installer la clé]**.

Une fois la clé publique installée, elle apparaît dans la liste. Vous pouvez utiliser le bouton **...** pour la télécharger ou copier son empreinte.

![](assets/gpg_install_download.png)

La clé peut être ensuite utilisée dans les workflows Adobe Campaign. Vous pouvez l’utiliser pour chiffrer des données lors de l’utilisation d’activités d’extraction de données.

![](assets/do-not-localize/how-to-video.png)[ Découvrez cette fonctionnalité en vidéo](#video)

Pour plus d’informations, consultez la documentation d’Adobe Campaign :

**Campaign v7/v8 :**

* [Compresser ou chiffrer un fichier](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html?lang=fr#getting-started)
* [Cas pratique : chiffrement et export de données à l’aide d’une clé installée sur le Panneau de contrôle](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=fr#use-case-gpg-encrypt)

**Campaign Standard:**

* [Gérer des données chiffrées](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=fr)
* [Cas pratique : chiffrement et export de données à l’aide d’une clé installée sur le Panneau de contrôle](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html?lang=fr#use-case-gpg-encrypt)

## Déchiffrement des données {#decrypting-data}

Le Panneau de contrôle permet de déchiffrer des données externes entrant dans vos instances Adobe Campaign.

Pour cela, vous devez générer une paire de clés GPG directement à partir du Panneau de contrôle.

* La **clé publique** sera partagée avec le système externe. Ce dernier l&#39;utilisera pour chiffrer les données à envoyer à Campaign.
* Campaign utilisera la **clé privée** pour déchiffrer les données chiffrées entrantes.

![](assets/do-not-localize/how-to-video.png)[ Découvrez cette fonctionnalité en vidéo](#video)

Pour générer une paire de clés dans le Panneau de contrôle, procédez comme suit :

1. Ouvrez la carte **[!UICONTROL Paramètres des instances]**, puis sélectionnez l’onglet **[!UICONTROL Clés GPS]** et l’instance Adobe Campaign souhaitée.

1. Cliquez sur le bouton **[!UICONTROL Générer la clé]**.

   ![](assets/gpg_generate.png)

1. Indiquez le nom de la clé, puis cliquez sur **[!UICONTROL Générer la clé]**. Ce nom vous permettra d’identifier la clé à utiliser pour le déchiffrement dans les workflows de Campaign.

   ![](assets/gpg_generate_name.png)

Une fois la paire de clés générée, la clé publique apparaît dans la liste. Notez que les paires de clés de déchiffrement sont générées sans date d’expiration.

Vous pouvez utiliser le bouton **...** pour télécharger la clé publique ou copier son empreinte.

![](assets/gpg_generate_list.png)

La clé publique peut être alors partagée avec tout système externe. Adobe Campaign pourra utiliser la clé privée dans les activités de chargement de données pour déchiffrer les données chiffrées à l’aide de la clé publique.

Pour plus d’informations, consultez la documentation d’Adobe Campaign :

**Campaign v7 et v8 :**

* [Décompresser ou déchiffrer un fichier avant traitement](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html?lang=fr)
* [Cas pratique : import de données chiffrées à l’aide d’une clé générée par le Panneau de contrôle](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html?lang=fr#use-case-gpg-decrypt)

**Campaign Standard:**

* [Gérer des données chiffrées](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=fr)
* [Cas pratique : import de données chiffrées à l’aide d’une clé générée par le Panneau de contrôle](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=fr#use-case-gpg-decrypt)

## Surveillance des clés GPG

Pour accéder aux clés GPG installées et générées pour vos instances, ouvrez la carte **[!UICONTROL Paramètres des instances]**, puis sélectionnez l’onglet **[!UICONTROL Clés GPG]**.

![](assets/gpg_list.png)

La liste contient toutes les clés GPG de chiffrement et de déchiffrement qui ont été installées et générées pour vos instances, avec des informations détaillées sur chaque clé :

* **[!UICONTROL Nom]** : nom défini lors de l’installation ou de la génération de la clé.
* **[!UICONTROL Cas pratique]** : cette colonne indique le cas pratique de la clé :

  ![](assets/gpg_icon_encrypt.png) : la clé a été installée pour le chiffrement des données.

  ![](assets/gpg_icon_decrypt.png) : la clé a été générée pour permettre le déchiffrement des données.

* **[!UICONTROL Empreinte]** : empreinte de la clé.
* **[!UICONTROL Expire]** : date d’expiration de la clé. Remarque : le Panneau de contrôle donne des indications visuelles à l’approche de sa date d’expiration :

   * Urgent (rouge) s’affiche 30 jours avant.
   * Avertissement (jaune) s’affiche 60 jours avant.
   * Une bannière rouge « Expirée » s’affiche une fois qu’une clé arrive à expiration.

  >[!NOTE]
  >
  >Aucune notification par email ne sera envoyée par le Panneau de contrôle.

Il est recommandé de supprimer toute clé dont vous n’avez plus besoin. Pour cela, cliquez sur le bouton **...**, puis sélectionnez **[!UICONTROL Supprimer la clé].**.

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>Avant de supprimer une clé, vérifiez qu’elle n’est utilisée dans aucun workflow Adobe Campaign pour éviter tout échec.

## Tutoriel vidéo {#video}

La vidéo ci-dessous explique comment générer et installer des clés GPG pour le chiffrement des données.

D’autres vidéos pratiques relatives à la gestion des clés GPG sont disponibles dans les pages de tutoriels [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=fr#instance-settings) et [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=fr#instance-settings).

>[!VIDEO](https://video.tv.adobe.com/v/36386?quality=12)
