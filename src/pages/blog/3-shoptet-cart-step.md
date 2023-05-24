---
title: "[3] Shoptet úpravy - Přídání 4. bodu kroku košíku "
excerpt: "Ornare cum cursus laoreet sagittis nunc fusce posuere per euismod dis vehicula a, semper fames lacus maecenas dictumst pulvinar neque enim non potenti. Torquent hac sociosqu eleifend potenti."
publishDate: "2023-02-04T11:39:36.050Z"
image: "https://github.com/janheder/janheder.cz/blob/main/src/assets/blog/thumb-sh-3.png?raw=true"
author: "Jan Heder"
layout: "@layouts/BlogLayout.astro"
---

> V této sérii článků sdílím užitečné tipy, návody a zkušenosti, jak lze rychle a jednoduše vylepšit váš eshop. 

Do navigace košíku přidá poslední bod "Dokončení objednávky"

Následující js vložte do patičky vašeho eshopu (popřípadě externího js souboru)

```js
if ($(".ordering-process").length){
    $(".cart-header").append('<li class="step step-4"><strong><span>Dokončení objednávky</span></strong></li>');
}
```
