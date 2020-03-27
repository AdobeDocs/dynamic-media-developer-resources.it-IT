---
description: Il tag Connector in server.xml supporta un attributo ciphers per limitare i caratteri che è possibile scegliere per una connessione SSL.
seo-description: Il tag Connector in server.xml supporta un attributo ciphers per limitare i caratteri che è possibile scegliere per una connessione SSL.
seo-title: Definizione dei caratteri SSL
solution: Experience Manager
title: Definizione dei caratteri SSL
topic: Scene7 Image Serving - Image Rendering API
uuid: 9490fb9a-5abb-4f5e-b660-b7af0a5e4b4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Definizione dei caratteri SSL{#defining-ssl-ciphers}

Il tag Connector in server.xml supporta un attributo ciphers per limitare i caratteri che è possibile scegliere per una connessione SSL.

Per impostazione predefinita, sono disponibili tutti i caratteri. L&#39;elenco è separato da virgole e può contenere uno dei seguenti valori:

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

Se uno dei valori è sbagliato, Tomcat abilita ogni singolo simbolo. È quindi essenziale controllare con uno strumento esterno dopo la configurazione per vedere quali caratteri sono effettivamente attivati.

Ad esempio, la seguente configurazione consente di abilitare solo le suite di cifratura a 128 bit e versioni successive:

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,SSL_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA,TLS_RSA_WITH_AES_128_CBC_SHA"`
