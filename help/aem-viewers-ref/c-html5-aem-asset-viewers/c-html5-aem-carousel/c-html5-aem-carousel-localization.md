---
title: Localizzazione di utente elementi dell'interfaccia
description: Alcuni contenuto visualizzati nel visualizzatore carosello sono soggetti a localizzazione. Questo include contenuto diapositiva pulsanti navigazione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 05f5abe0-1124-4114-864d-440699bcdc39
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Localizzazione di utente elementi dell&#39;interfaccia{#localization-of-user-interface-elements}

Alcuni contenuti visualizzati nel visualizzatore carosello sono soggetti a localizzazione. Questo contenuto include pulsanti di spostamento tra le diapositive.

Ogni contenuto testuale del visualizzatore che può essere localizzato è rappresentato dallo speciale identificatore SDK per visualizzatori denominato SYMBOL. A qualsiasi SYMBOL è associato un valore di testo predefinito per una lingua Inglese ( `"en"`) fornita con la visualizzatore predefinita e può anche avere valori definiti in utente per tutte le impostazioni internazionali necessarie.

All&#39;avvio del visualizzatore, viene controllata la lingua corrente per verificare se esiste un valore definito da utente per ogni SYMBOL supportato per tale impostazione. Se esiste, utilizza il valore utente-defined; In caso contrario, viene utilizzato il testo predefinito predefinito.

I dati di localizzazione definiti dall&#39;utente possono essere passati all&#39;visualizzatore come oggetto JSON di localizzazione. Tale oggetto contiene l&#39;elenco delle impostazioni internazionali supportate, i valori di testo SYMBOL per ogni lingua e le impostazioni internazionali predefinite.

Un esempio di tale oggetto di localizzazione è il seguente:

```
{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left", 
"PanRightButton.TOOLTIP":"Right" 
 }, 
 "fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste", 
"PanRightButton .TOOLTIP":"Droit" 
}, 
defaultLocale:"en" 
}
```

Nell&#39;esempio precedente, l&#39;oggetto di localizzazione definisce due impostazioni internazionali ( `"en"` e `"fr"`) e fornisce la localizzazione per due utente elementi dell&#39;interfaccia in ogni lingua.

Il codice della pagina Web deve passare l&#39;oggetto di localizzazione al costruttore visualizzatore, come valore di `localizedTexts` campo dell&#39;oggetto di configurazione. Un&#39;opzione alternativa consiste nel passare l&#39;oggetto di localizzazione chiamando `setLocalizedTexts(localizationInfo)` il metodo.

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
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>La riproduzione selezionata mette in pausa pulsante stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>La riproduzione non selezionata mette in pausa pulsante stato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO </span> </p> </td> 
   <td colname="col2"> <p> Descrizione comandi ed etichetta ARIA per pulsanti diapositiva precedente e successivo. </p> <p>Accetta due token sostitutivi: <span class="codeph"> $CURRENT_FRAME$ </span> per l'indice diapositiva corrente e <span class="codeph"> $TOTAL_FRAMES$ </span> per il numero totale di diapositive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Contenitore.ETICHETTA </span> </p> </td> 
   <td colname="col2"> <p> Etichetta ARIA per l’elemento visualizzatore di primo livello. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p> Descrizione del ruolo ARIA per il componente della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p> Suggerimenti per l'utilizzo di ARIA per gli utenti di tastiera. </p> </td> 
  </tr> 
 </tbody> 
</table>
