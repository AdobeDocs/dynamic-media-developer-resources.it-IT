---
description: Il tag Connector nel server.xml supporta un attributo ciphers per limitare i crittografie che possono essere scelte per una connessione SSL.
solution: Experience Manager
title: Definizione dei codici SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# Definizione dei crittografi SSL{#defining-ssl-ciphers}

Il tag Connector nel server.xml supporta un attributo ciphers per limitare i crittografie che possono essere scelte per una connessione SSL.

Per impostazione predefinita sono disponibili tutte le crittografie. L’elenco è separato da virgole e può contenere uno dei seguenti valori:

`SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_DSS_WITH_DES_CBC_SHA`

`SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_RSA_EXPORT_WITH_RC4_40_MD5`

`SSL_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

`TLS_RSA_WITH_AES_128_CBC_SHA`

Se uno qualsiasi dei valori è sbagliato, Tomcat consentirà ogni singolo segno. Quindi è essenziale controllare con uno strumento esterno dopo la configurazione per vedere quali crittografie sono effettivamente abilitate.

Ad esempio, la seguente configurazione abilita solo le suite di cifratura a 128 bit e successive:

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,SSL_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA,TLS_RSA_WITH_AES_128_CBC_SHA"`
