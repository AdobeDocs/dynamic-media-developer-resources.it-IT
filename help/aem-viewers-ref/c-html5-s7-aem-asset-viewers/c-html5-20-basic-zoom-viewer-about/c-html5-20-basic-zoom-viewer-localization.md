---
title: Localizzazione degli elementi dell’interfaccia utente
description: Alcuni contenuti visualizzati in Basic Zoom Viewer (Visualizzatore zoom di base) sono soggetti alla localizzazione, inclusi i pulsanti di zoom e un pulsante a schermo intero.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 8c399b64-e278-41bc-a9eb-692812979fea
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Localizzazione degli elementi dell’interfaccia utente{#localization-of-user-interface-elements}

Alcuni contenuti visualizzati in Basic Zoom Viewer (Visualizzatore zoom di base) sono soggetti alla localizzazione, inclusi i pulsanti di zoom e un pulsante a schermo intero.

Ogni contenuto testuale nel visualizzatore che può essere localizzato è rappresentato da uno speciale identificatore SDK del visualizzatore chiamato SYMBOL. Qualsiasi simbolo ha un valore di testo associato di default per la lingua inglese ( `"en"`) fornito con il visualizzatore predefinito e può anche avere valori definiti dall&#39;utente impostati per tutte le impostazioni internazionali necessarie.

All&#39;avvio, il visualizzatore controlla le impostazioni locali correnti per verificare se è presente un valore definito dall&#39;utente per ciascun SIMBOLO supportato nelle impostazioni locali. In caso affermativo, viene utilizzato il valore definito dall’utente; in caso contrario, viene utilizzato il testo predefinito.

I dati di localizzazione definiti dall’utente possono essere trasmessi al visualizzatore come oggetto JSON di localizzazione. Tale oggetto contiene l&#39;elenco delle impostazioni locali supportate, i valori di testo SYMBOL per ciascuna impostazione locale e le impostazioni locali predefinite.

Un esempio di tale oggetto di localizzazione:

```
{ 
"en":{ 
"CloseButton.TOOLTIP":"Close", 
"ZoomInButton.TOOLTIP":"Zoom In" 
 }, 
 "fr":{ 
"CloseButton.TOOLTIP":"Fermer", 
"ZoomInButton.TOOLTIP":"Agrandir" 
}, 
defaultLocale:"en" 
}
```

Nell&#39;esempio precedente, l&#39;oggetto di localizzazione definisce due impostazioni internazionali ( `"en"` e `"fr"`) e fornisce la localizzazione per due elementi dell&#39;interfaccia utente in ciascuna lingua.

Il codice della pagina web deve trasmettere tale oggetto di localizzazione al costruttore del visualizzatore come valore di `localizedTexts` dell&#39;oggetto di configurazione. In alternativa, è possibile passare l’oggetto di localizzazione chiamando `setLocalizedTexts(localizationInfo)` metodo.

Sono supportati i seguenti SIMBOLI:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SIMBOLO </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione comando per... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>Etichetta ARIA per l’elemento visualizzatore di primo livello. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del ruolo ARIA del componente della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>Suggerimenti per l’utilizzo di ARIA per gli utenti che utilizzano la tastiera. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Pulsante Chiudi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Pulsante Zoom in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Pulsante Zoom out. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Pulsante di ripristino zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>pulsante a schermo intero in stato normale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>pulsante di visualizzazione a schermo intero. </p> </td> 
  </tr> 
 </tbody> 
</table>
