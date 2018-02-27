# craft.variants

## How to get variants

Usually you will only want to retrieve products, giving you access to their variants. Sometimes you might want to query for variants directly.

You can access your site’s variants from your templates via `craft.variants`
It returns an [ElementQuery](https://github.com/craftcms/docs/blob/v3/en/element-queries.md) object.

```twig
{% set variants = craft.variants.id(8376).one() %}

{{ variant.sku }} - {{ variant.salePrice }}
```

## Parameters

`craft.variants` supports the following parameters:

### ID
The variant's element ID.

### productId
The product ID this variant belongs to.

### sku
The variant's SKU

### default
Whether the variant is the product's default variant

Accepts: boolean (`true` or `false`)

### stock
The stock amount

Accepts: integer

### hasStock
Whether the variant has unlimited stock or stock greater than zero.

Accepts: boolean (`true` or `false`)