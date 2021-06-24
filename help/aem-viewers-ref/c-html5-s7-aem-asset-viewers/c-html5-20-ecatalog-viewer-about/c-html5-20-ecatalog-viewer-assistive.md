---
description: Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
title: Supporto tecnologico per assistenza
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog,Accessibilità
role: Developer,Business Practitioner
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Supporto tecnologico per assistenza{#assistive-technology-support}

Tutti i componenti visualizzatore supportano ruoli e attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

Per impostazione predefinita, l’elemento visualizzatore di livello principale ha l’attributo ruolo `region` e `aria-label` impostato sul nome del visualizzatore. Puoi controllare l’etichetta con il simbolo di localizzazione `Container.LABEL` .

I pulsanti hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label` . Il valore dell&#39;attributo `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disabilitato, l&#39;attributo `aria-disabled` viene impostato di conseguenza.

La vista principale ha il ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito dal simbolo di localizzazione `ROLE_DESCRIPTION` del componente di visualizzazione principale corrispondente. I suggerimenti per la navigazione degli utenti tramite tastiera vengono forniti utilizzando `aria-describedby`, il testo per il suggerimento di utilizzo proviene dal simbolo di localizzazione `USAGE_HINT` . Se una risorsa ha un’etichetta definita nel campo UserData , l’attributo `aria-label` viene impostato con il valore di tale etichetta.

Le aree calde, le aree geografiche e le mappe immagine hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label` , con il valore dell&#39;etichetta di area sensibile o mappa immagine. Quando l&#39;utente mette a fuoco punti o mappe immagine, i suggerimenti per la navigazione degli utenti tramite tastiera vengono forniti utilizzando `aria-describedby`, con il testo per il suggerimento di utilizzo proveniente dal simbolo di localizzazione `USAGE_HINT`.

Le miniature hanno il ruolo `dialog` con l’attributo `aria-label` controllato dal simbolo di localizzazione `ThumbnailGridView.LABEL` . Le singole miniature hanno il ruolo `button`. Se è selezionata una miniatura, l’attributo `aria-selected` viene impostato su `true`.

I componenti che visualizzano i campioni hanno il ruolo `listbox` con l’attributo `aria-label` impostato sul valore del simbolo di localizzazione `LABEL` di quel componente. I singoli campioni hanno il ruolo `option` con gli attributi `aria-setsize` e `aria-posinset` per descrivere la posizione del campione nel set. Se è selezionato un campione, l’attributo `aria-selected` viene impostato su `true`.

Gli elenchi a discesa sono attivati dai pulsanti con l’attributo `aria-haspopup` aggiuntivo impostato su `true` e l’attributo `aria-controls` che fa riferimento all’elemento del pannello a discesa effettivo. Il pannello a discesa stesso ha il ruolo `menu` con elementi secondari con il ruolo `menuitem`. Per ogni voce di menu è specificato l&#39;attributo `aria-label` .

Le finestre di dialogo modali hanno il ruolo `dialog`. L&#39;attributo `aria-labelledby` fa riferimento all&#39;elemento di intestazione della finestra di dialogo.
