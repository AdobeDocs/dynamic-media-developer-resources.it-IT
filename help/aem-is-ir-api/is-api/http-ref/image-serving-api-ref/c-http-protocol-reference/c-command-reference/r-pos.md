---
title: pos
description: Posizione livello.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
TQID: 'https://experienceleague.adobe.com/9UMGN0TeM4mZ0IZI--dEA3KBYKOVhJxCJMZuPevlq8o'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 2%

---

# pos{#pos}

Posizione livello.

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Offset pixel dall'origine di questo livello all'origine del livello 0 (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>Scostamento normalizzato dall'origine di questo livello all'origine del livello 0 (reale, reale). </p></td> 
 </tr> 
</table>

Se sono presenti livelli immagine, testo e colore tinta unita, `pos=` specifica la posizione di un ancoraggio livello rispetto all&#39;ancoraggio livello 0. I valori delle coordinate `posN=` sono normalizzati rispetto alle dimensioni effettive del livello 0.

Se sono presenti livelli di effetto, `pos=` sposta il livello di effetto rispetto al livello padre.

I valori positivi spostano il livello verso destra/basso e i valori negativi verso sinistra/alto. In `posN=0.5,0.5`, il livello viene spostato di metà della larghezza e dell&#39;altezza del livello 0 verso il basso e verso destra.

## Proprietà {#section-51a60cdc52d040538fef378ace7c2e7d}

Attributo livello. Ignorato se `layer=0` o `layer=comp`.

## Predefinito {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. Questa coordinata posiziona l&#39;ancoraggio del livello nella stessa posizione dell&#39;ancoraggio del livello 0 se si tratta di un livello di immagine, testo o colore a tinta unita. Posiziona un livello effetto direttamente sopra o sotto il relativo livello padre.

## Esempio {#section-a89a02c22f6b4260bfcf7c842cd6069d}

Vedi l&#39;esempio A in [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-812d95575ba542808e8387d0a8650606}

[origin= origine](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
