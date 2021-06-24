---
description: Usa queste impostazioni del server per SSL.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---

# SSL{#ssl}

Usa queste impostazioni del server per SSL.

## TC::SslPort - Porta di ascolto {#section-c80eb582bf684b3fa7313a77cc606769}

Specifica la porta di ascolto per Platform Server per le connessioni SSL. Il valore predefinito è 8443.

## TC::keystoreFile - Percorso file keystore {#section-0cdf9b3cfcf249818b22221d01bafebe}

Specifica il percorso/nome del file dell&#39;archivio chiavi SSL. Può essere un percorso assoluto o relativo a [!DNL *[!DNL install_folder]*/conf]. Il valore predefinito è *install_folder*/conf/scene7keystore.

## TC::keystorePass - Password keystore {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

Password del file dell&#39;archivio chiavi. Il valore predefinito è `scene7`.

## TC::keystoreType - Keystore Type {#section-8f263e1ba67740728cd39181960d7c7d}

Selezionare il tipo di archivio chiavi. Sono supportati i valori &#39; `Java'` (predefinito) e &#39; `PKCS12`&#39;.
