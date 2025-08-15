---
title: Localizzazione degli elementi dell’interfaccia utente
description: Alcuni contenuti visualizzati nel Visualizzatore video sono soggetti a localizzazione. Questo contenuto include descrizioni con gli strumenti per gli elementi dell’interfaccia utente e un messaggio di errore visualizzato quando il video non può essere riprodotto.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 4748d04e-7f9d-413f-9e9a-a0fad129c5fc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# Localizzazione degli elementi dell’interfaccia utente{#localization-of-user-interface-elements}

Alcuni contenuti visualizzati nel Visualizzatore video sono soggetti a localizzazione. Questo contenuto include descrizioni con gli strumenti per gli elementi dell’interfaccia utente e un messaggio di errore visualizzato quando il video non può essere riprodotto.

Ogni contenuto testuale del visualizzatore che può essere localizzato è rappresentato da uno speciale identificatore SDK del visualizzatore denominato SYMBOL. Qualsiasi simbolo ha un valore di testo associato predefinito per le impostazioni locali inglesi ( `"en"`) fornito con il visualizzatore predefinito. Può inoltre disporre di valori definiti dall&#39;utente impostati per il numero di impostazioni internazionali necessario.

All&#39;avvio, il visualizzatore controlla le impostazioni locali correnti per verificare se è presente un valore definito dall&#39;utente per ciascun SIMBOLO supportato per le impostazioni locali. In caso affermativo, viene utilizzato il valore definito dall’utente; in caso contrario, viene utilizzato il testo predefinito.

I dati di localizzazione definiti dall’utente possono essere trasmessi al visualizzatore come oggetto JSON di localizzazione. Tale oggetto contiene l&#39;elenco delle impostazioni locali supportate, i valori di testo SYMBOL per ciascuna impostazione locale e le impostazioni locali predefinite.

Un esempio di tale oggetto di localizzazione è il seguente:

```
{ 
"en":{ 
"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Play" 
 }, 
 "fr":{ 
"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Jouer" 
}, 
defaultLocale:"en" 
}
```

Nell&#39;esempio precedente, l&#39;oggetto di localizzazione definisce due impostazioni locali ( `"en"` e `"fr"`) e fornisce la localizzazione per due elementi dell&#39;interfaccia utente in ciascuna impostazione locale.

Il codice della pagina Web deve trasmettere tale oggetto di localizzazione al costruttore del visualizzatore come valore del campo `localizedTexts` dell&#39;oggetto di configurazione. In alternativa, passare l&#39;oggetto di localizzazione chiamando il metodo `setLocalizedTexts(localizationInfo)`.

Sono supportati i seguenti SIMBOLI:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SIMBOLO </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p> Etichetta ARIA per l’elemento visualizzatore di primo livello. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Descrizione dello stato selezionato del pulsante Pausa di riproduzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comando per lo stato deselezionato del pulsante Riproduci pausa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_REPLAY </span> </p> </td> 
   <td colname="col2"> <p>Descrizione dello stato del pulsante Pausa di riproduzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comando per lo scorrimento video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comando per la durata del video sulla barra di controllo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comando per lo stato del volume modificabile selezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comando per il volume mutabile deselezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME </span> </p> </td> 
   <td colname="col2"> <p> Etichetta della manopola del cursore del volume esposta tramite l’attributo aria-valuetext <span class="codeph"> di ARIA </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Descrizione dello stato selezionato per il pulsante a schermo intero. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Descrizione dello stato deselezionato del pulsante a schermo intero. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comando per lo stato selezionato del pulsante sottotitoli. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comando per lo stato deselezionato del pulsante sottotitoli. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comando per lo strumento di condivisione social. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante di condivisione e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Descrizione dell’intestazione della finestra di dialogo e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante di chiusura in alto a destra della finestra di dialogo e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.INVALID_ADDRESSS </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del messaggio di errore visualizzato in caso di formato non corretto dell’indirizzo e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Condivisione e-mail <span class="codeph">.TO </span> </p> </td> 
   <td colname="col2"> <p>Etichetta per il campo di input "A". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ADD </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante Aggiungi un altro indirizzo e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Condivisione e-mail.AGGIUNGI </span> </p> </td> 
   <td colname="col2"> <p>Didascalia del pulsante Aggiungi un altro indirizzo e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Condivisione e-mail <span class="codeph">.DA </span> </p> </td> 
   <td colname="col2"> <p>Etichetta per il campo di input "Da". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Condivisione e-mail.MESSAGGIO </span> </p> </td> 
   <td colname="col2"> <p>Etichetta per il campo di input "Messaggio". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_REMOVE </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante Rimuovi indirizzo e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Condivisione e-mail.ANNULLA </span> </p> </td> 
   <td colname="col2"> <p>Didascalia del pulsante Annulla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante Annulla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Condivisione e-mail.CHIUDI </span> </p> </td> 
   <td colname="col2"> <p>Didascalia del pulsante Chiudi visualizzata nella parte inferiore della finestra di dialogo dopo l’invio del modulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante Chiudi visualizzato nella parte inferiore della finestra di dialogo dopo l’invio del modulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Didascalia del pulsante di invio del modulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante di invio del modulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Condivisione e-mail.SEND_SUCCESS </span> </p> </td> 
   <td colname="col2"> <p>Messaggio di conferma visualizzato quando l’e-mail è stata inviata correttamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_FAILURE </span> </p> </td> 
   <td colname="col2"> <p>Messaggio di errore visualizzato quando l’e-mail non è stata inviata correttamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante di condivisione da incorporare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comando per l'intestazione della finestra di dialogo Incorpora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> IncorporaShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante di chiusura superiore destro della finestra di dialogo Incorpora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del testo del codice di incorporamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.EMBED_SIZE </span> </p> </td> 
   <td colname="col2"> <p>Etichetta per la casella combinata dimensione incorporamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CondivisioneIncorporata.ANNULLA </span> </p> </td> 
   <td colname="col2"> <p>Didascalia del pulsante Annulla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante Annulla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Didascalia del pulsante Seleziona tutto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AZIONE EmbedShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante Seleziona tutto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE </span> </p> </td> 
   <td colname="col2"> <p>Testo per l'ultima voce "custom size" (dimensione personalizzata) nella casella combinata embed size (dimensione incorporata). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante Condivisione collegamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comando per l'intestazione della finestra di dialogo Collega. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comando per il pulsante di chiusura superiore destro della finestra di dialogo Collega. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del collegamento di condivisione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ANNULLA </span> </p> </td> 
   <td colname="col2"> <p>Didascalia del pulsante Annulla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante Annulla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Didascalia del pulsante Seleziona tutto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AZIONE LINKShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante Seleziona tutto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante Condividi di Facebook. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante Condividi di Twitter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoPlayer.ERRORE </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del messaggio di errore visualizzato quando non è possibile riprodurre il video. </p> </td> 
  </tr> 
 </tbody> 
</table>
