---
title: "[2] Shoptet úpravy - Hlídací pes produktu ve výpisu kategorie"
excerpt: "Ornare cum cursus laoreet sagittis nunc fusce posuere per euismod dis vehicula a, semper fames lacus maecenas dictumst pulvinar neque enim non potenti. Torquent hac sociosqu eleifend potenti."
publishDate: "2023-01-28T11:39:36.050Z"
image: "https://github.com/janheder/janheder.cz/blob/main/src/assets/blog/thumb-sh-2.png?raw=true"
author: "Jan Heder"
layout: "@layouts/BlogLayout.astro"
---

> V této sérii článků sdílím užitečné tipy, návody a zkušenosti, jak lze rychle a jednoduše vylepšit váš eshop. 


```javascript
function productCardEdit(){ 

  if ($(".product").length){
          $(".product .p-bottom > div[data-micro-availability='https://schema.org/OutOfStock']").each(function(){
              let productUrl = $(this).parents(".product").find(".image").attr("href").slice(0, -1);
              $(this).parents(".product").find(".pr-action").attr("id","product-detail-form");
              $(this).parents(".product").find(".image").prepend('<a href="'+ productUrl +':hlidat-cenu/" class="link-icon watchdog btn" title="Hlídat cenu" rel="nofollow">Hlídat</a>');
          });

          $(".p-tools .watchdog").click(function(){
              $(".product .pr-action").attr("id","");
              $(this).parents(".product").find(".pr-action").attr("id","product-detail-form");
          });
  }

}


productCardEdit();

document.addEventListener('ShoptetDOMPageContentLoaded', function () {
    productCardEdit();
});
document.addEventListener('ShoptetDOMPageMoreProductsLoaded', function () {
    productCardEdit();
});

```


```css


```