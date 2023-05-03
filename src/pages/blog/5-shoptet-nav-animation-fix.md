---
title: "[5] Shoptet úpravy - Oprava animace otevírání menu na mobilu"
excerpt: "Ornare cum cursus laoreet sagittis nunc fusce posuere per euismod dis vehicula a, semper fames lacus maecenas dictumst pulvinar neque enim non potenti. Torquent hac sociosqu eleifend potenti."
publishDate: "2023-02-18T11:39:36.050Z"
image: "https://github.com/janheder/janheder.cz/blob/main/src/assets/blog/thumb-sh-5.png?raw=true"
author: "Jan Heder"
layout: "@layouts/BlogLayout.astro"
---

Následující css vložte do hlavičky vašeho eshopu

```css
@media (max-width: 767px){
    #navigation {
        transform: translateX(100%);
        max-width: 100%;
        width: 300px;
    }
    .navigation-in>ul>li{
        flex-shrink: 0;
    }
    .navigation-window-visible #navigation {
        transform: translateX(0%);
        max-width: 100%;
        width: 300px;
    }
}
```