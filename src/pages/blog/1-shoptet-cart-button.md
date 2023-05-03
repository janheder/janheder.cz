---
title: "[1] Shoptet úpravy - Změna textace tlačítka objednat v košíku"
excerpt: "Ornare cum cursus laoreet sagittis nunc fusce posuere per euismod dis vehicula a, semper fames lacus maecenas dictumst pulvinar neque enim non potenti. Torquent hac sociosqu eleifend potenti."
publishDate: "2023-01-21T11:39:36.050Z"
image: "https://github.com/janheder/janheder.cz/blob/main/src/assets/blog/thumb-sh-1.png?raw=true"
author: "Jan Heder"
layout: "@layouts/BlogLayout.astro"
---

> V této sérii článků sdílím užitečné tipy, návody a zkušenosti, jak lze rychle a jednoduše vylepšit váš eshop. 

Následující css vložte do hlavičky vašeho eshopu

```css
#submit-order .order-button-text{
    font-size: 0;
}
#submit-order .order-button-text::after{
    content: "Potvrdit nákup";
    font-size: initial;
}
#submit-order .order-button-suffix{
    display: none;
}
```




