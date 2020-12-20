---
description: Utilizzate queste impostazioni del server per SSL.
seo-description: Utilizzate queste impostazioni del server per SSL.
seo-title: SSL
solution: Experience Manager
title: SSL
topic: Scene7 Image Serving - Image Rendering API
uuid: dec9bd09-8191-4010-8898-2890ffbe9ca7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---


# SSL{#ssl}

Utilizzate queste impostazioni del server per SSL.

## TC::SslPort - Porta di ascolto {#section-c80eb582bf684b3fa7313a77cc606769}

Specifica la porta di ascolto per il server piattaforma per le connessioni SSL. Il valore predefinito è 8443.

## TC::keystoreFile - Percorso file archivio chiavi {#section-0cdf9b3cfcf249818b22221d01bafebe}

Specificate il percorso/nome del file dell’archivio di chiavi SSL. Può essere un percorso assoluto o un percorso relativo a [!DNL *[!DNL install_folder]*/conf]. Il valore predefinito è *install_folder*/conf/scene7keystore.

## TC::keystorePass - Password archivio chiavi {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

La password per il file keystore. Il valore predefinito è `scene7`.

## TC::keystoreType - Keystore Type {#section-8f263e1ba67740728cd39181960d7c7d}

Selezionare il tipo di archivio di chiavi. &#39; `Java'` (predefinito) e &#39; `PKCS12`&#39; sono supportati.
