---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: b792cddb-f3d2-4609-95b7-105d76fb3d6f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 1%

---

# InfoPanelPopup.template{#infopanelpopup-template}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`modello`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> modello</span></span> </p> </td> 
   <td> <p>Il modello per contenuto in cui vengono uniti i dati restituiti dal server informazioni. </p> <p>Il modello di contenuto è un XML che segue questa DTD: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;&lbrack;
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      &rbrack;&gt;</code> </p> <p>La sintassi effettiva del modello di contenuto è la seguente: </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]&gt;
      &lt;!&lbrack;CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]&gt;
      &lt;/info&gt;</code> </p> <p>Il modello deve iniziare con l'elemento <span class="codeph"> &lt;info&gt;</span> che può contenere <span class="codeph"> &lt;var&gt;</span> elementi predefiniti facoltativi. Il contenuto del modello stesso, <span class="codeph"> TEMPLATE_CONTENT</span>, è un testo HTML. Inoltre, il modello di contenuto può contenere nomi di variabili racchiusi tra <span class="codeph"> $</span> caratteri. Questi caratteri vengono sostituiti con i valori delle variabili restituiti dal server informazioni o con quelli predefiniti. </p> <p>Le variabili predefinite definite nel modello possono essere globali (se l’attributo di rollover non è impostato) o specifiche per una determinata chiave di rollover (se l’attributo di rollover è presente). </p> <p>Durante l’elaborazione dei modelli, le variabili specifiche per le chiavi di rollover hanno la precedenza rispetto alle variabili globali. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Tenere presente che quando si configura Info Panel Popup, il codice HTML e il codice JavaScript passato al Pannello informazioni vengono eseguiti sul computer del client. Di conseguenza, assicurati che tale codice HTML e il codice JavaScript siano protetti.

## Proprietà {#section-6dd7785357d740d095fa9f7fd0f67da4}

Facoltativo.

## Predefinito {#section-cd5db06d08aa4de49e37d6c938b41570}

Nessuno.

## Esempio {#section-16d184665c484964af9a22f79ff3f840}

Supponendo che la risposta del server informazioni restituisca il nome del prodotto come variabile `$1$` e che l&#39;URL dell&#39;immagine del prodotto venga restituito come variabile `$2$`.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
