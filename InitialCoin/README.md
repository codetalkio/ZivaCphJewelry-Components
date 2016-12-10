# Initial Coin

General information for adding a customization field is located at https://docs.shopify.com/manual/configuration/store-customization/page-specific/product-page/get-customization-information-for-products.

## Description

The idea is to allow the user to visualize the design of their necklace (Initial Coin), before buying it. The design the user has chosen is then attached to the order, so that no extra communication is needed to actually create the custom design afterwards.

Idea | Final Implementation
:---:|:---:
![Original Idea](https://raw.githubusercontent.com/codetalkio/ZivaCphJewelry-Components/master/InitialCoin/Design/original-idea.png) | ![Final Implementation](https://raw.githubusercontent.com/codetalkio/ZivaCphJewelry-Components/master/InitialCoin/Design/final-implementation.png)

## Images

Under `Settings` -> `Files` -> `Upload Files`.

* Upload all files from `Images` directly into the root (there aren't folders anyways)

## Theme

Under `Online Store`, press the `...` and choose `Edit HTML/CSS`.

* Add assets
    * Assets/initial-coin.js.liquid
    * Assets/initial-coin.scss.liquid
* Add snippet with coin stuff (depending on the theme)
    * Brooklyn Theme
        * Create a new snippet with the name "initial-coin-components.liquid" and add the contents to `Snippets/initial-coin-components.liquid`
    * Pipeline Theme
        * Create a new snippet with the name "product-initial-coin-components.liquid" and add the contents to `Snippets/initial-coin-components.liquid`
        * Create a new snippet with the name "product-initial-coint.liquid" and add the contents to the `Snippets/product-initial-coint.liquid`
* Add the product template
    * Create a new template for "product" with the name "coin" and add the contents to `Templates/product.coin.liquid`

## Product

Under `Products` either `Add Product` or change an existing product, and then set the following options.

* Theme templates: product.coin
* Variants
    * Material: Goldplated, Sterling Silver
    * Gems: 0, 1, 2, 3, 4
    * Each variant should have an image matching their material
    * In total this should give 10 variants
* SKU:
    * Gold: `g0`, `g1`, `g2`, `g3` and `g4`
    * Silver: `s0`, `s1`, `s2`, `s3` and `s4`
