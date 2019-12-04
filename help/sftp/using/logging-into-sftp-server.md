---
title: Connexion à votre serveur SFTP
description: Découvrez comment vous connecter à votre serveur SFTP
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# Connexion à votre serveur SFTP {#logging-into-sft-server}

Les étapes ci-dessous expliquent comment connecter votre serveur SFTP via votre application cliente SFTP.

Avant de vous connecter au serveur, vérifiez les points suivants :

* Your SFTP server is **hosted by Adobe**.
* Votre **nom d’utilisateur** a été configuré pour le serveur. You can check this information directly in the Control Panel, in the **Key management** tab from the SFTP Card.
* Vous disposez d'une **paire de clés privée et publique** pour vous connecter au serveur SFTP. Refer to [this section](../../sftp/using/key-management.md) for more on how to add the SSH key.
* Votre **adresse IP publique a été whitelistée** sur le serveur SFTP. If not, refer to [this section](../../sftp/using/ip-range-whitelisting.md) for more on how to whitelist your IP range.
* You have an access to a **SFTP client software**. Vous pouvez consulter votre service informatique pour connaître l'application cliente SFTP qu'il vous recommande d'utiliser, ou en rechercher une sur Internet si les politiques de votre entreprise le permettent.

Pour vous connecter à votre serveur SFTP, procédez comme suit :

1. Launch the Control Panel, then select the **[!UICONTROL Key Management]** tab from the **[!UICONTROL SFTP]** card.

   ![](assets/fingerprintNEW2.png)

1. Lancez l’application cliente SFTP, puis copiez-collez l’adresse du serveur à partir du Panneau de configuration, suivi de "campaign.adobe.com", puis indiquez votre nom d’utilisateur.

   ![](assets/connect1.png)

1. Dans le champ **[!UICONTROL Clé privée SSH], sélectionnez le fichier de clé privée stocké sur votre ordinateur.** Il correspond à un fichier texte portant le même nom que votre clé publique, sans l'extension ".pub" (par exemple, "enable").

   ![](assets/connect2.png)

   Le champ **[!UICONTROL Mot de passe]est automatiquement renseigné avec la clé du fichier.**

   ![](assets/connect3.png)

   Vous pouvez vérifier que la clé que vous essayez d’utiliser est enregistrée dans le Panneau de configuration en comparant l’empreinte de la clé privée ou publique à l’empreinte des clés figurant dans l’onglet Gestion des clés de la carte SFTP.

   ![](assets/fingerprint3.png)

   >[!NOTE]
   >
   >Si vous utilisez un ordinateur Mac, vous pouvez afficher l’empreinte de la clé privée stockée sur votre ordinateur en exécutant la commande suivante :
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. Une fois toutes les informations indiquées, cliquez sur **[!UICONTROL Connexion]pour vous connecter à votre serveur SFTP.**

   ![](assets/sftpconnected.png)
