---
title: "[6] Shoptet úpravy - Tlačítko nahoru"
excerpt: "Ornare cum cursus laoreet sagittis nunc fusce posuere per euismod dis vehicula a, semper fames lacus maecenas dictumst pulvinar neque enim non potenti. Torquent hac sociosqu eleifend potenti."
publishDate: "2023-03-04T11:39:36.050Z"
image: "https://github.com/janheder/janheder.cz/blob/main/src/assets/blog/thumb-sh-6.png?raw=true"
author: "Jan Heder"
layout: "@layouts/BlogLayout.astro"
---

Následující css vložte do hlavičky vašeho eshopu (popřípadě externího css souboru)

```css
#backToTop {
    display: none;
}

@media (max-width: 991px) {
    #backToTop {
        position: fixed;
        opacity: 1;
        pointer-events: auto;
        bottom: 15px;
        right: 15px;
        background: gray;
        color: white;
        font-size: 11px;
        height: 46px;
        width: 46px;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        z-index: 9;
        transition: 0.3s ease opacity;
    }
    #backToTop span {
        border: solid white;
        border-width: 0 2px 2px 0;
        display: inline-block;
        padding: 3px;
        transform: rotate(-135deg);
        margin-top: 4px;
    }
}
```

Následující js vložte do patičky vašeho eshopu (popřípadě externího js souboru)

```javascript
    $(document).ready(function() {
        let windowHeight = $(window).height();
        let docHeight = $(document).height();
        let multiplier = 4;

        if((windowHeight * multiplier) < docHeight){
            $("body").append("<div id='backToTop' aria-label='Scrollovat nahoru'><span></span></div>");

            document.querySelector('#backToTop').addEventListener('click', e => {
                window.scrollTo({top: 0, behavior: 'smooth'});
            },{
                passive: true
            });
        }
    });
```