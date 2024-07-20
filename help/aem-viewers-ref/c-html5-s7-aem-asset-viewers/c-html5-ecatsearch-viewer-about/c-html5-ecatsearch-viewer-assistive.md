---
description: Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
title: Supporto di tecnologie assistive
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search,Accessibility
role: Developer,User
exl-id: fbfc9415-6ab8-466c-9a1f-d33565eff2a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Supporto di tecnologie assistive{#assistive-technology-support}

Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

L&#39;elemento visualizzatore di primo livello ha il ruolo `region` e l&#39;attributo `aria-label` impostati per impostazione predefinita sul nome del visualizzatore. È possibile controllare l&#39;etichetta con il simbolo di localizzazione `Container.LABEL`.

I pulsanti hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label`. Il valore dell&#39;attributo `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disattivato, l&#39;attributo `aria-disabled` viene impostato di conseguenza.

La visualizzazione principale ha il ruolo `application`. In `aria-roledescription` viene fornita una breve descrizione della visualizzazione principale, con il valore definito dal simbolo di localizzazione `ROLE_DESCRIPTION` del componente della visualizzazione principale corrispondente. Gli hint di navigazione per gli utenti che utilizzano la tastiera vengono forniti utilizzando `aria-describedby`. Il testo dell&#39;hint di utilizzo proviene dal simbolo di localizzazione `USAGE_HINT`. Se per una risorsa è definita un&#39;etichetta nel campo UserData, l&#39;attributo `aria-label` viene impostato con il valore di tale etichetta.

I punti attivi, le aree geografiche e le mappe immagine hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label`, con il valore del punto attivo o dell&#39;etichetta della mappa immagine. Quando l&#39;utente mette a fuoco gli hot spot o le mappe immagine, gli hint di navigazione per gli utenti della tastiera vengono forniti utilizzando `aria-describedby`, con il testo per l&#39;hint di utilizzo proveniente dal simbolo di localizzazione `USAGE_HINT`.

Le miniature hanno il ruolo `dialog` con attributo `aria-label` controllato dal simbolo di localizzazione `ThumbnailGridView.LABEL`. Le singole miniature hanno il ruolo `button`. Se è selezionata una miniatura, l&#39;attributo `aria-selected` viene impostato su `true`.

I componenti che visualizzano i campioni hanno il ruolo `listbox` con l&#39;attributo `aria-label` impostato sul valore del simbolo di localizzazione `LABEL` di quel componente. I singoli campioni hanno il ruolo `option` con gli attributi `aria-setsize` e `aria-posinset` per descrivere la posizione del campione nel set. Se è selezionato un campione, l&#39;attributo `aria-selected` viene impostato su `true`.

Gli elenchi a discesa vengono attivati da pulsanti con l&#39;attributo aggiuntivo `aria-haspopup` impostato su `true` e l&#39;attributo `aria-controls` che fa riferimento all&#39;elemento effettivo del pannello a discesa. Il pannello a discesa stesso ha il ruolo `menu` con elementi secondari che hanno il ruolo `menuitem`. Per ogni voce di menu è specificato l&#39;attributo `aria-label`.

L&#39;interfaccia utente di ricerca è raggruppata nell&#39;elemento con il ruolo `search`. Il campo di input della ricerca ha il ruolo `searchbox` e fa riferimento all&#39;etichetta informativa controllata dal simbolo di localizzazione `SearchPanel.INFO_PROMPT` con l&#39;attributo `aria-describedby`.

Le finestre di dialogo modali hanno il ruolo `dialog`. L&#39;attributo `aria-labelledby` fa riferimento all&#39;elemento intestazione della finestra di dialogo.
