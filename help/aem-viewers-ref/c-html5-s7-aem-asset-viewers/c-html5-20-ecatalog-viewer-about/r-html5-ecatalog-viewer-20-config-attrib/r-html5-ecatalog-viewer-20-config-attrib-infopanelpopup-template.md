---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 2%

---


# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`template`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> template</span></span> </p> </td> 
   <td> <p>Il modello di contenuto in cui vengono uniti i dati restituiti dal server di informazioni. </p> <p>Il modello di contenuto è un XML che segue questa DTD: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>La sintassi effettiva per il modello di contenuto è la seguente: </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>In altre parole, il modello deve iniziare con l'elemento <span class="codeph"> &lt;info&gt;</span> che può contenere elementi <span class="codeph"> &lt;var&gt;</span> facoltativi predefiniti. Il contenuto del modello stesso, <span class="codeph"> TEMPLATE_CONTENT</span> è testo HTML. Inoltre, il modello di contenuto può contenere nomi di variabili racchiusi tra <span class="codeph"> $</span> che vengono sostituiti con i valori delle variabili restituiti dal server informazioni o con quelli predefiniti. </p> <p>Le variabili predefinite definite nel modello possono essere globali (se l’attributo rollover non è impostato) o specifiche per un determinato tasto rollover (se è presente l’attributo rollover). </p> <p>Durante l’elaborazione dei modelli le variabili specifiche per il passaggio al passaggio del mouse hanno la precedenza sulle variabili globali. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Tieni presente che quando configuri Info Panel Popup, il codice HTML e il codice JavaScript passato al pannello Info viene eseguito sul computer del client. Assicurati pertanto che tali codici HTML e codice JavaScript siano protetti.

## Proprietà {#section-6dd7785357d740d095fa9f7fd0f67da4}

Facoltativo.

## Predefinito {#section-cd5db06d08aa4de49e37d6c938b41570}

Nessuno.

## Esempio {#section-16d184665c484964af9a22f79ff3f840}

Supponendo che la risposta del server informazioni restituisca il nome del prodotto come variabile `$1$` e che l&#39;URL dell&#39;immagine del prodotto venga restituito come variabile `$2$`.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
