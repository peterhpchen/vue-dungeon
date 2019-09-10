# 在探險之前

只要有使用 Vue.js 寫程式的，應該大部分的人都有使用 Single File Component (簡稱：SFC) 開發元件，SFC 會像是下面這樣：

```html
<template>
  <div class="example">{{ msg }}</div>
</template>

<script>
export default {
  data () {
    return {
      msg: 'Hello world!'
    }
  }
}
</script>

<style>
.example {
  color: red;
}
</style>

<custom1>
  This could be e.g. documentation for the component.
</custom1>
```

它會是由多個不同功能的區塊組成 (`template`, `script`, `style`...) ，並存在以 `vue` 為副檔名的檔案中。

由這單個 `vue` 檔，我們就可以定義一個元件所需的全部：配置 (`template`) ，邏輯 (`script`) ，樣式 (style) 。

SFC 簡潔且優雅的設計是我愛上 Vue.js 的很重要的原因之一。

## 為什麼是這個題目

當我在專案的每一處使用著 SFC 時，漸漸習慣並且視這樣的方式為常，直到這次的鐵人賽，當我在想題目時，才想到 SFC 設計背後會有什麼樣驚奇的東西可以學習呢？也因此我開始了這次的冒險。

## 為什麼要研究原始碼

記得以前在學校學習數學時，老師一定都會教你如何推導公式，而不是直接叫你背公式，雖然最後學到的都是公式，但本質上卻有很大的不同，在推導公式的過程中我們所學到的更多，記憶也更加的深刻。

程式碼也是一樣的，能理解某個怎麼使用是很棒的，可是如果能了解其背後的原理，能學到的並不只是這個功能的實作而已，還可以學到實作這個功能的功能的實作，這樣你理解了某個功能的原理，可能學會了幾倍多的功能，更加深了程式的功力。

## 為什麼不從 vue.js 核心庫開始研究

Vue.js core 中有許多 Javascript 的進階使用方式，對於想要在 Javascript 上有更深鑽研的人是非常受用的，但對於想要先精進 Vue.js 能力的人來說就有點太深了，經由研究 Vue.js 的旁枝系統，對 Vue.js 的開發可以有更深的幫助，也不會花太多的時間在 Javascript 上。

## 前置技能

在開始觀看本系列文前，需要擁有下面的基礎知識：

* Vue.js 基本使用能力
* Webpack 基本使用能力
* Babel 的認識
* PostCSS 的認識

上面的都是擁有基礎知識即可，較深入的我們會在文章中講解。

## 概述

本系列會先講解在解析原始碼之前所需的必要知識，接著深入講解原始碼，最後將解析原始碼時所學的東西應用到專案中。

### 探索之前 (5篇)

從 SFC 的基本介紹講起，到 Webpack loader 及 plugin 的開發，PostCSS plugin 的原理，在解析源碼前做一個完整的導讀。

### 解析原始碼 (20篇)

從 vue-loader 原始碼說起，由外而內講解 SFC 的建置過程。

### 學習到的東西 (5篇)

將前兩部分所學到的技術應用在專案上，發揮所學。

## 附註

* 文章中若有解釋不到位甚至是錯誤的情形發生，還請各位大大指導。
* 在每篇文章的最後會附上參考資料，若在文章中有引用到其他大大的文章也會盡量詳細的說明，若是有遺漏之處，還請點出。
* 本文章會同步於 [GitHub](https://github.com/peterhpchen/vue-dungeon) 上。
