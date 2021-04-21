---
description: Richiedi convalida.
solution: Experience Manager
title: validate
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
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

Analizza la stringa di richiesta come se fosse stato specificato `req=img`, ma senza sostituire le variabili e valutare gli oggetti di riferimento (immagini, profili ICC, font e così via). Se l’analisi non riesce, viene restituita la risposta di errore standard. In caso contrario viene restituita la seguente proprietà:

`request.isValid=1`

La risposta HTTP non è memorizzabile nella cache.

Le richieste che supportano il formato di risposta JSONP ti consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
