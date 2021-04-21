---
description: Alcuni contenuti visualizzati nel Visualizzatore video sono soggetti a localizzazione. Questo contenuto include le descrizioni comandi degli elementi dell’interfaccia utente e un messaggio di errore visualizzato quando il video non può essere riprodotto.
solution: Experience Manager
title: Localizzazione degli elementi dell’interfaccia utente
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 0%

---


# Localizzazione degli elementi dell&#39;interfaccia utente{#localization-of-user-interface-elements}

Alcuni contenuti visualizzati nel Visualizzatore video sono soggetti a localizzazione. Questo contenuto include le descrizioni comandi degli elementi dell’interfaccia utente e un messaggio di errore visualizzato quando il video non può essere riprodotto.

Ogni contenuto testuale nel visualizzatore che può essere localizzato è rappresentato da uno speciale identificatore SDK del visualizzatore denominato SYMBOL. A qualsiasi SIMBOLO è associato un valore di testo predefinito per le impostazioni internazionali inglesi ( `"en"`) fornito con il visualizzatore predefinito. Può anche avere valori definiti dall&#39;utente impostati per tutte le impostazioni internazionali necessarie.

All’avvio del visualizzatore, controlla le impostazioni internazionali correnti per vedere se esiste un valore definito dall’utente per ogni SYMBOL supportato per le impostazioni internazionali. In caso affermativo, utilizza il valore definito dall’utente; in caso contrario, torna al testo predefinito preconfigurato.

I dati di localizzazione definiti dall&#39;utente possono essere trasmessi al visualizzatore come oggetto JSON di localizzazione. Tale oggetto contiene l&#39;elenco delle impostazioni internazionali supportate, i valori di testo SYMBOL per ciascuna impostazione internazionale e le impostazioni internazionali predefinite.

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

Nell’esempio precedente, l’oggetto di localizzazione definisce due impostazioni internazionali ( `"en"` e `"fr"`) e fornisce la localizzazione di due elementi dell’interfaccia utente in ciascuna impostazione internazionale.

Il codice della pagina web deve passare tale oggetto di localizzazione al costruttore del visualizzatore come valore del campo `localizedTexts` dell&#39;oggetto di configurazione. Un&#39;opzione alternativa consiste nel passare l&#39;oggetto di localizzazione chiamando il metodo `setLocalizedTexts(localizationInfo)` .

Sono supportati i seguenti SYMBOL:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SIMBOLO </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p> Etichetta ARIA per l’elemento visualizzatore di livello superiore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per lo stato selezionato del pulsante di pausa di riproduzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per lo stato del pulsante di pausa di riproduzione deselezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_REPLAY  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per lo stato del pulsante di pausa di riproduzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per lo scorrimento video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per il tempo video sulla barra di controllo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MeableVolume.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per lo stato del volume mutabile selezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MablesVolume.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per il volume mutabile deselezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MablesVolume.TOOLTIP_VOLUME  </span> </p> </td> 
   <td colname="col2"> <p> Etichetta della manopola del dispositivo di scorrimento del volume esposta mediante l'attributo ARIA <span class="codeph"> aria-value </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per lo stato del pulsante a schermo intero selezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per lo stato del pulsante a schermo intero deselezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per lo stato del pulsante per la didascalia chiusa selezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per lo stato del pulsante di didascalia chiusa deselezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per lo strumento di condivisione social network. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per il pulsante di condivisione e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi dell’intestazione della finestra di dialogo e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi del pulsante di chiusura superiore destro della finestra di dialogo e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.INVALID_ADDRESSS  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi del messaggio di errore visualizzato nel caso in cui l’indirizzo e-mail non sia corretto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TO  </span> </p> </td> 
   <td colname="col2"> <p>Etichetta per il campo di input "To". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ADD  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi del pulsante "Aggiungi un altro indirizzo e-mail". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ADD  </span> </p> </td> 
   <td colname="col2"> <p>Didascalia del pulsante "Aggiungi un altro indirizzo e-mail". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.FROM  </span> </p> </td> 
   <td colname="col2"> <p>Etichetta per il campo di input "Da". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.MESSAGE  </span> </p> </td> 
   <td colname="col2"> <p>Etichetta per il campo di input "Messaggio". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_REMOVE  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per il pulsante "Rimuovi indirizzo e-mail". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Didascalia del pulsante "Annulla". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per il pulsante "Annulla". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Didascalia del pulsante di chiusura visualizzato nella parte inferiore della finestra di dialogo dopo l’invio del modulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi del pulsante Chiudi visualizzato nella parte inferiore della finestra di dialogo dopo l’invio del modulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Didascalia del pulsante di invio del modulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per il pulsante di invio del modulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_SUCCESS  </span> </p> </td> 
   <td colname="col2"> <p>Messaggio di conferma visualizzato quando l’e-mail è stata inviata correttamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_FAILURE  </span> </p> </td> 
   <td colname="col2"> <p>Messaggio di errore visualizzato quando l’e-mail non è stata inviata correttamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per il pulsante di incorporamento condivisione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per l'intestazione della finestra di dialogo di incorporamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per il pulsante di chiusura superiore destro della finestra di dialogo di incorporamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del testo del codice di incorporamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.EMBED_SIZE  </span> </p> </td> 
   <td colname="col2"> <p>Etichetta per la casella combinata Dimensione di incorporamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Didascalia del pulsante "Annulla". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per il pulsante "Annulla". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Didascalia per il pulsante "Seleziona tutto". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AZIONE EmbedShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante Seleziona tutto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE  </span> </p> </td> 
   <td colname="col2"> <p>Testo per l’ultima voce "dimensione personalizzata" nella casella combinata Dimensione incorporamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per il pulsante di condivisione del collegamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi dell’intestazione della finestra di dialogo del collegamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi del pulsante di chiusura superiore destro della finestra di dialogo di collegamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del collegamento di condivisione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Didascalia del pulsante "Annulla". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi per il pulsante "Annulla". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Didascalia per il pulsante "Seleziona tutto". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AZIONE LinkShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante Seleziona tutto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante di condivisione Facebook. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione del pulsante di condivisione Twitter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoPlayer.ERROR  </span> </p> </td> 
   <td colname="col2"> <p>Descrizione comandi del messaggio di errore visualizzato quando non è possibile riprodurre il video. </p> </td> 
  </tr> 
 </tbody> 
</table>

