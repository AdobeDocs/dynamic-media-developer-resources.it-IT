---
description: Usa queste impostazioni server per SSL.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 3%

---

# SSL{#ssl}

Usa queste impostazioni server per SSL.

## TC::SslPort - Porta di ascolto {#section-c80eb582bf684b3fa7313a77cc606769}

Specifica la porta di ascolto per [!DNL Platform Server] per le connessioni SSL. Il valore predefinito è 8443.

## TC::keystoreFile - Percorso file registro chiavi {#section-0cdf9b3cfcf249818b22221d01bafebe}

Specifica il percorso/nome del file del keystore SSL. Può essere un percorso assoluto o relativo a [!DNL *[!DNL install_folder]*/conf]. Il valore predefinito è *install_folder*/conf/scene7keystore.

## TC::keystorePass - Password keystore {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

La password per il file keystore. Il valore predefinito è `scene7`.

## TC::keystoreType - Tipo keystore {#section-8f263e1ba67740728cd39181960d7c7d}

Seleziona il tipo di keystore. Sono supportati &#39; `Java'` (impostazione predefinita) e &#39; `PKCS12`&#39;.
