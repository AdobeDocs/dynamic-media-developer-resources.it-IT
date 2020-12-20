---
description: Richiedi convalida.
seo-description: Richiedi convalida.
seo-title: validate
solution: Experience Manager
title: validate
topic: Scene7 Image Serving - Image Rendering API
uuid: 5322c484-2cf5-4022-9863-73fc525beb56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---


# validate{#validate}

Richiedi convalida.

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>Identificatore univoco della richiesta. </p></td> 
 </tr> 
</table>

Analizza la stringa di richiesta come se fosse stato specificato `req=img`, ma senza sostituire le variabili e valutare gli oggetti di riferimento (immagini, profili ICC, font e così via). Se l&#39;analisi non riesce, viene restituita la risposta di errore standard. In caso contrario viene restituita la seguente proprietà:

`request.isValid=1`

La risposta HTTP non è memorizzabile nella cache.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
