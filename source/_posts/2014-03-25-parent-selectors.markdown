---
layout: post
title: "Sass - Parent Selectors"
date: 2014-03-25 13:42:42 +0200
comments: true
categories: sass
---
### Sass'da seçiciler için stil yazarken, class isimlerinin gereksiz tekrarını engellemek için kullandığımız bir kaç yöntem var.

Birincisi link seçicilerinde kullandığımız &: ikilisi. a sınıfında efekt kullanacağımız zaman bu işimizi kolayşaltırıyor.

Örnek sass kodu:



      a
        font-weight: bold
        text-decoration: none
        &:hover
          text-decoration: underline




Css çıktısı:

      a {
        font-weight: bold;
        text-decoration: none; }
        a:hover {
                 text-decoration: underline;}


İkinci kullanımı daha temiz ve amacına uygun. &- bu iki karekter bir üst sınıfın adını çağırıyor.

Örnek sass kodu:

            #main
              color: black
              &-sidebar
                border: 1px solid

Css çıktısı:

        #main {
          color: black; }
          #main-sidebar {
            border: 1px solid; }