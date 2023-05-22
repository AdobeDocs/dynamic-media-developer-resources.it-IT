---
title: Supporto di tecnologie assistive
description: Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images,Accessibility
role: Developer,User
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Supporto di tecnologie assistive{#assistive-technology-support}

Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

L’elemento visualizzatore di primo livello ha il ruolo `region` e `aria-label` attributo impostato per impostazione predefinita sul nome del visualizzatore. Puoi controllare l’etichetta con `Container.LABEL` simbolo di localizzazione.

La visualizzazione principale ha un ruolo `application`. Una breve descrizione della vista principale è fornita in `aria-roledescription`, con il valore definito da `ROLE_DESCRIPTION` simbolo di localizzazione del componente della vista principale corrispondente. Gli hint di navigazione per gli utenti che utilizzano la tastiera sono forniti tramite `aria-describedby`, il testo per l’hint di utilizzo proviene da `USAGE_HINT` simbolo di localizzazione. Se per una risorsa è stata definita un’etichetta nel campo UserData, il `aria-label` viene impostato con il valore di tale etichetta.

I punti attivi, le aree geografiche e le mappe immagine hanno il ruolo `button` e set di testo descrittivo con `aria-label` con il valore dell&#39;area sensibile o dell&#39;etichetta della mappa immagine. Quando l’utente mette a fuoco gli hot spot o le mappe immagine, vengono forniti suggerimenti di navigazione per gli utenti che utilizzano la tastiera utilizzando `aria-describedby`, con il testo per l’hint di utilizzo proveniente dalla sezione `USAGE_HINT` simbolo di localizzazione.
