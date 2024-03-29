---
title: InfoPanelPopup.template
description: InfoPanelPopup.template
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 20618017-2f73-4951-baa9-2063a0f4efcb
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 2%

---

# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`modello`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> modello</span></span> </p> </td> 
   <td> <p>Il modello per contenuto in cui vengono uniti i dati restituiti dal server informazioni. </p> <p>Il modello di contenuto è un XML che segue questa DTD: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>La sintassi effettiva del modello di contenuto è la seguente: </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>Il modello deve iniziare con <span class="codeph"> &lt;info&gt;</span> elemento che può contenere valori predefiniti facoltativi <span class="codeph"> &lt;var&gt;</span> elementi. Il contenuto del modello stesso, <span class="codeph"> CONTENUTO_MODELLO</span> è il testo HTML. Inoltre, il modello di contenuto può contenere nomi di variabili racchiusi in <span class="codeph"> $</span> caratteri sostituiti con i valori delle variabili restituiti dal server informazioni o con quelli predefiniti. </p> <p>Le variabili predefinite definite nel modello possono essere globali (se l’attributo di rollover non è impostato) o specifiche per una determinata chiave di rollover (se l’attributo di rollover è presente). </p> <p>Durante l’elaborazione dei modelli, le variabili specifiche per le chiavi di rollover hanno la precedenza rispetto alle variabili globali. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Quando si configura il popup del pannello Info, il codice HTML e il codice JavaScript passato al pannello Info vengono eseguiti sul computer del client. Di conseguenza, assicurati che tale codice HTML e il codice JavaScript siano sicuri.

## Proprietà {#section-6dd7785357d740d095fa9f7fd0f67da4}

Facoltativo.

## Predefinito {#section-cd5db06d08aa4de49e37d6c938b41570}

Nessuno.

## Esempio {#section-16d184665c484964af9a22f79ff3f840}

Supponendo che la risposta del server informazioni restituisca il nome del prodotto come variabile `$1$` L’URL dell’immagine del prodotto e viene restituito come variabile `$2$`.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
