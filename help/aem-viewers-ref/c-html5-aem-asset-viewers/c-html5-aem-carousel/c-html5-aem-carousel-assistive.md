---
description: Tutti i componenti del visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l'integrazione con tecnologie di supporto come gli assistenti vocali.
seo-description: Tutti i componenti del visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l'integrazione con tecnologie di supporto come gli assistenti vocali.
seo-title: Supporto per tecnologie di assistenza
solution: Experience Manager
title: Supporto per tecnologie di assistenza
topic: Dynamic Media
uuid: 72b414f4-b647-4afa-a409-a8ba90227d3f
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---


# Supporto per la tecnologia di assistenza{#assistive-technology-support}

Tutti i componenti del visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l&#39;integrazione con tecnologie di supporto come gli assistenti vocali.

Per impostazione predefinita, l’elemento visualizzatore di livello principale ha l’attributo ruolo `region` e `aria-label` impostato sul nome del visualizzatore. È possibile controllare l&#39;etichetta con il simbolo di localizzazione `Container.LABEL`.

I pulsanti hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label`. Il valore dell&#39;attributo `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disattivato, l&#39;attributo `aria-disabled` viene impostato di conseguenza.

I pulsanti che consentono di spostarsi tra le diapositive carosello contengono etichette che vengono aggiornate in fase di esecuzione a seconda della diapositiva attualmente selezionata. Il modello per l&#39;etichetta di questo pulsante è impostato con il simbolo di localizzazione `CAROUSELVIEWER_TOOLTIP_GOTO`.

La vista principale ha il ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito dal simbolo di localizzazione `ROLE_DESCRIPTION` del componente di visualizzazione principale corrispondente. I suggerimenti di navigazione per gli utenti della tastiera sono forniti utilizzando `aria-describedby`, il testo per il suggerimento sull&#39;utilizzo proviene dal simbolo di localizzazione `USAGE_HINT`. Se una risorsa ha un&#39;etichetta definita nel campo UserData, l&#39;attributo `aria-label` viene impostato con il valore di tale etichetta.

Le aree sensibili, le aree geografiche e le mappe immagine hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label`, con il valore dell&#39;etichetta di area sensibile o mappa immagine. Quando l&#39;utente mette a fuoco aree sensibili o mappe immagine, i suggerimenti di navigazione per gli utenti della tastiera sono forniti utilizzando `aria-describedby`, con il testo per il suggerimento sull&#39;utilizzo proveniente dal simbolo di localizzazione `USAGE_HINT`.
