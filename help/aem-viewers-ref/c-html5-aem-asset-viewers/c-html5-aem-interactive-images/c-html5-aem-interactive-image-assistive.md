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

L&#39;elemento visualizzatore di primo livello ha il ruolo `region` e l&#39;attributo `aria-label` impostati per impostazione predefinita sul nome del visualizzatore. È possibile controllare l&#39;etichetta con il simbolo di localizzazione `Container.LABEL`.

La visualizzazione principale ha il ruolo `application`. In `aria-roledescription` viene fornita una breve descrizione della visualizzazione principale, con il valore definito dal simbolo di localizzazione `ROLE_DESCRIPTION` del componente della visualizzazione principale corrispondente. Gli hint di navigazione per gli utenti che utilizzano la tastiera vengono forniti utilizzando `aria-describedby`. Il testo dell&#39;hint di utilizzo proviene dal simbolo di localizzazione `USAGE_HINT`. Se per una risorsa è definita un&#39;etichetta nel campo UserData, l&#39;attributo `aria-label` viene impostato con il valore di tale etichetta.

I punti attivi, le aree geografiche e le mappe immagine hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label`, con il valore del punto attivo o dell&#39;etichetta della mappa immagine. Quando l&#39;utente mette a fuoco gli hot spot o le mappe immagine, gli hint di navigazione per gli utenti della tastiera vengono forniti utilizzando `aria-describedby`, con il testo per l&#39;hint di utilizzo proveniente dal simbolo di localizzazione `USAGE_HINT`.
