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

L&#39;elemento visualizzatore di primo livello ha il ruolo `region` e l&#39;attributo `aria-label` impostati per impostazione predefinita sul nome del visualizzatore. È possibile controllare l&#39;etichetta con il simbolo di localizzazione `Container.LABEL`.

I pulsanti hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label`. Il valore dell&#39;attributo `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disabilitato, l&#39;attributo `aria-disabled` viene impostato di conseguenza.

I pulsanti che consentono di spostarsi tra le diapositive del carosello presentano etichette aggiornate in fase di esecuzione a seconda della diapositiva attualmente selezionata. Il modello per questa etichetta di pulsanti è impostato con il simbolo di localizzazione `CAROUSELVIEWER_TOOLTIP_GOTO`.

La visualizzazione principale ha il ruolo `application`. In `aria-roledescription` viene fornita una breve descrizione della visualizzazione principale, con il valore definito dal simbolo di localizzazione `ROLE_DESCRIPTION` del componente della visualizzazione principale corrispondente. Gli hint di navigazione per gli utenti che utilizzano la tastiera vengono forniti utilizzando `aria-describedby`. Il testo dell&#39;hint di utilizzo proviene dal simbolo di localizzazione `USAGE_HINT`. Se per una risorsa è definita un&#39;etichetta nel campo UserData, l&#39;attributo `aria-label` viene impostato con il valore di tale etichetta.

I punti attivi, le aree geografiche e le mappe immagine hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label`, con il valore del punto attivo o dell&#39;etichetta della mappa immagine. Quando l&#39;utente mette a fuoco gli hot spot o le mappe immagine, gli hint di navigazione per gli utenti della tastiera vengono forniti utilizzando `aria-describedby`, con il testo per l&#39;hint di utilizzo proveniente dal simbolo di localizzazione `USAGE_HINT`.
