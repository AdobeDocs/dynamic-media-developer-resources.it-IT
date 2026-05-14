---
title: Supporto di tecnologie assistive
description: Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video,Accessibility
role: Developer,User
exl-id: e0652730-60ee-41db-890b-e223b279e47d
TQID: 'https://experienceleague.adobe.com/wOJ59nhF2lMgcT4L8-Qn2PwkVHGYKwTaKR0y1VDtjOY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 181
ht-degree: 0%

---

# Supporto di tecnologie assistive{#assistive-technology-support}

Tutti i componenti visualizzatore supportano i ruoli e gli attributi ARIA (Accessible Rich Internet Applications) per migliorare l’integrazione con tecnologie per l’accessibilità, come gli assistenti vocali.

L&#39;elemento visualizzatore di primo livello ha il ruolo `region` e l&#39;attributo `aria-label` impostati per impostazione predefinita sul nome del visualizzatore. È possibile controllare l&#39;etichetta con il simbolo di localizzazione `Container.LABEL`.

I pulsanti hanno il ruolo `button` e il testo descrittivo impostato con l&#39;attributo `aria-label`. Il valore dell&#39;attributo `aria-label` viene popolato dal valore del simbolo di localizzazione del pulsante. Quando un pulsante è disabilitato, l&#39;attributo `aria-disabled` viene impostato di conseguenza.

I componenti cursore hanno il ruolo `slider` con gli attributi `aria-valuenow`, `aria-valuemin` e `aria-valuemax` per descrivere la posizione corrente del cursore.

Gli elenchi a discesa vengono attivati da pulsanti con l&#39;attributo aggiuntivo `aria-haspopup` impostato su `true` e l&#39;attributo `aria-controls` che fa riferimento all&#39;elemento effettivo del pannello a discesa. Il pannello a discesa ha il ruolo `menu` con sottoelementi che hanno il ruolo `menuitem`. Per ogni voce di menu è specificato l&#39;attributo `aria-label`.

Le finestre di dialogo modali hanno il ruolo `dialog`. L&#39;attributo `aria-labelledby` fa riferimento all&#39;elemento intestazione della finestra di dialogo.
