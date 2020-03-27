---
description: Tutti i componenti del visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l'integrazione con tecnologie di supporto come gli assistenti vocali.
seo-description: Tutti i componenti del visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l'integrazione con tecnologie di supporto come gli assistenti vocali.
seo-title: Supporto per tecnologie di assistenza
solution: Experience Manager
title: Supporto per tecnologie di assistenza
topic: Dynamic media
uuid: 72b414f4-b647-4afa-a409-a8ba90227d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Supporto per tecnologie di assistenza{#assistive-technology-support}

Tutti i componenti del visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l&#39;integrazione con tecnologie di supporto come gli assistenti vocali.

Per impostazione predefinita, l’elemento visualizzatore di livello principale ha ruolo `region` e `aria-label` attributo impostati sul nome del visualizzatore. È possibile controllare l&#39;etichetta con il simbolo di `Container.LABEL` localizzazione.

I pulsanti hanno il ruolo `button` e il testo descrittivo impostato con `aria-label` attributo. Il valore dell&#39; `aria-label` attributo viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disattivato, l&#39; `aria-disabled` attributo viene impostato di conseguenza.

I pulsanti che consentono di spostarsi tra le diapositive carosello contengono etichette che vengono aggiornate in fase di esecuzione a seconda della diapositiva attualmente selezionata. Il modello per l&#39;etichetta di questo pulsante è impostato con il simbolo di `CAROUSELVIEWER_TOOLTIP_GOTO` localizzazione.

La visione principale ha un ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito dal simbolo di `ROLE_DESCRIPTION` localizzazione del componente di visualizzazione principale corrispondente. I suggerimenti di navigazione per gli utenti della tastiera vengono forniti utilizzando `aria-describedby`, il testo per il suggerimento di utilizzo viene dal simbolo di `USAGE_HINT` localizzazione. Se una risorsa ha un&#39;etichetta definita nel campo UserData, l&#39; `aria-label` attributo è impostato con il valore di tale etichetta.

Le aree sensibili, le aree geografiche e le mappe immagine hanno il ruolo `button` e il testo descrittivo impostato con `aria-label` l&#39;attributo, con il valore dell&#39;etichetta di area sensibile o mappa immagine. Quando l&#39;utente mette a fuoco aree sensibili o mappe immagine, vengono forniti suggerimenti di navigazione per gli utenti della tastiera, `aria-describedby`con il testo del suggerimento relativo all&#39;utilizzo che proviene dal simbolo di `USAGE_HINT` localizzazione.
