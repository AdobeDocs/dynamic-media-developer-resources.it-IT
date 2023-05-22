---
title: Supporto di tecnologie assistive
description: Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners,Accessibility
role: Developer,User
exl-id: 3ed943e8-4695-4561-9be0-1b6ed30294f8
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# Supporto di tecnologie assistive{#assistive-technology-support}

Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

L’elemento visualizzatore di primo livello ha il ruolo `region` e `aria-label` attributo impostato per impostazione predefinita sul nome del visualizzatore. Puoi controllare l’etichetta con `Container.LABEL` simbolo di localizzazione.

I pulsanti hanno il ruolo `button` e set di testo descrittivo con `aria-label` attributo. Il valore di `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disattivato, `aria-disabled` viene impostato di conseguenza.

I pulsanti che consentono di spostarsi tra le diapositive del carosello presentano etichette aggiornate in fase di esecuzione a seconda della diapositiva attualmente selezionata. Il modello per l&#39;etichetta di questi pulsanti è impostato con `CAROUSELVIEWER_TOOLTIP_GOTO` simbolo di localizzazione.

La visualizzazione principale ha un ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito da `ROLE_DESCRIPTION` simbolo di localizzazione del componente della vista principale corrispondente. Gli hint di navigazione per gli utenti che utilizzano la tastiera sono forniti tramite `aria-describedby`, il testo per l’hint di utilizzo proviene da `USAGE_HINT` simbolo di localizzazione. Se per una risorsa è stata definita un’etichetta nel campo UserData, il `aria-label` viene impostato con il valore di tale etichetta.

I punti attivi, le aree geografiche e le mappe immagine hanno il ruolo `button` e set di testo descrittivo con `aria-label` con il valore dell&#39;area sensibile o dell&#39;etichetta della mappa immagine. Quando l’utente mette a fuoco gli hot spot o le mappe immagine, vengono forniti suggerimenti di navigazione per gli utenti che utilizzano la tastiera utilizzando `aria-describedby`, con il testo per l’hint di utilizzo proveniente dalla sezione `USAGE_HINT` simbolo di localizzazione.
