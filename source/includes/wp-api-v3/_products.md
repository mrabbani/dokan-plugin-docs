# Products #

The products API allows you to create, view, update, and delete individual, or a batch, of products.

## Product properties ##

| Attribute               | Type      | Description                                                                                                          |
|-------------------------|-----------|----------------------------------------------------------------------------------------------------------------------|
| `id`                    | integer   | Unique identifier for the resource. <i class="label label-info">read-only</i>                                        |
| `name`                  | string    | Product name.                                                                                                        |
| `slug`                  | string    | Product slug.                                                                                                        |
| `permalink`             | string    | Product URL. <i class="label label-info">read-only</i>                                                               |
| `date_created`          | date-time | The date the product was created, in the site's timezone. <i class="label label-info">read-only</i>                  |
| `date_created_gmt`      | date-time | The date the product was created, as GMT. <i class="label label-info">read-only</i>                                  |
| `date_modified`         | date-time | The date the product was last modified, in the site's timezone. <i class="label label-info">read-only</i>            |
| `date_modified_gmt`     | date-time | The date the product was last modified, as GMT. <i class="label label-info">read-only</i>                            |
| `type`                  | string    | Product type. Options: `simple`, `grouped`, `external` and `variable`. Default is `simple`.                          |
| `status`                | string    | Product status (post status). Options: `draft`, `pending`, `private` and `publish`. Default is `publish`.            |
| `featured`              | boolean   | Featured product. Default is `false`.                                                                                |
| `catalog_visibility`    | string    | Catalog visibility. Options: `visible`, `catalog`, `search` and `hidden`. Default is `visible`.                      |
| `description`           | string    | Product description.                                                                                                 |
| `short_description`     | string    | Product short description.                                                                                           |
| `sku`                   | string    | Unique identifier.                                                                                                   |
| `price`                 | string    | Current product price. <i class="label label-info">read-only</i>                                                     |
| `regular_price`         | string    | Product regular price.                                                                                               |
| `sale_price`            | string    | Product sale price.                                                                                                  |
| `date_on_sale_from`     | date-time | Start date of sale price, in the site's timezone.                                                                    |
| `date_on_sale_from_gmt` | date-time | Start date of sale price, as GMT.                                                                                    |
| `date_on_sale_to`       | date-time | End date of sale price, in the site's timezone.                                                                      |
| `date_on_sale_to_gmt`   | date-time | End date of sale price, as GMT.                                                                                      |
| `price_html`            | string    | Price formatted in HTML. <i class="label label-info">read-only</i>                                                   |
| `on_sale`               | boolean   | Shows if the product is on sale. <i class="label label-info">read-only</i>                                           |
| `purchasable`           | boolean   | Shows if the product can be bought. <i class="label label-info">read-only</i>                                        |
| `total_sales`           | integer   | Amount of sales. <i class="label label-info">read-only</i>                                                           |
| `virtual`               | boolean   | If the product is virtual. Default is `false`.                                                                       |
| `downloadable`          | boolean   | If the product is downloadable. Default is `false`.                                                                  |
| `downloads`             | array     | List of downloadable files. See [Product - Downloads properties](#product-downloads-properties)                      |
| `download_limit`        | integer   | Number of times downloadable files can be downloaded after purchase. Default is `-1`.                                |
| `download_expiry`       | integer   | Number of days until access to downloadable files expires. Default is `-1`.                                          |
| `external_url`          | string    | Product external URL. Only for external products.                                                                    |
| `button_text`           | string    | Product external button text. Only for external products.                                                            |
| `tax_status`            | string    | Tax status. Options: `taxable`, `shipping` and `none`. Default is `taxable`.                                         |
| `tax_class`             | string    | Tax class.                                                                                                           |
| `manage_stock`          | boolean   | Stock management at product level. Default is `false`.                                                               |
| `stock_quantity`        | integer   | Stock quantity.                                                                                                      |
| `stock_status`          | string    | Controls the stock status of the product. Options: `instock`, `outofstock`, `onbackorder`. Default is `instock`.     |
| `backorders`            | string    | If managing stock, this controls if backorders are allowed. Options: `no`, `notify` and `yes`. Default is `no`.      |
| `backorders_allowed`    | boolean   | Shows if backorders are allowed. <i class="label label-info">read-only</i>                                           |
| `backordered`           | boolean   | Shows if the product is on backordered. <i class="label label-info">read-only</i>                                    |
| `sold_individually`     | boolean   | Allow one item to be bought in a single order. Default is `false`.                                                   |
| `weight`                | string    | Product weight.                                                                                                      |
| `dimensions`            | object    | Product dimensions. See [Product - Dimensions properties](#product-dimensions-properties)                            |
| `shipping_required`     | boolean   | Shows if the product need to be shipped. <i class="label label-info">read-only</i>                                   |
| `shipping_taxable`      | boolean   | Shows whether or not the product shipping is taxable. <i class="label label-info">read-only</i>                      |
| `shipping_class`        | string    | Shipping class slug.                                                                                                 |
| `shipping_class_id`     | integer   | Shipping class ID. <i class="label label-info">read-only</i>                                                         |
| `reviews_allowed`       | boolean   | Allow reviews. Default is `true`.                                                                                    |
| `average_rating`        | string    | Reviews average rating. <i class="label label-info">read-only</i>                                                    |
| `rating_count`          | integer   | Amount of reviews that the product have. <i class="label label-info">read-only</i>                                   |
| `related_ids`           | array     | List of related products IDs. <i class="label label-info">read-only</i>                                              |
| `upsell_ids`            | array     | List of up-sell products IDs.                                                                                        |
| `cross_sell_ids`        | array     | List of cross-sell products IDs.                                                                                     |
| `parent_id`             | integer   | Product parent ID.                                                                                                   |
| `purchase_note`         | string    | Optional note to send the customer after purchase.                                                                   |
| `categories`            | array     | List of categories. See [Product - Categories properties](#product-categories-properties)                            |
| `tags`                  | array     | List of tags. See [Product - Tags properties](#product-tags-properties)                                              |
| `images`                | array     | List of images. See [Product - Images properties](#product-images-properties)                                        |
| `attributes`            | array     | List of attributes. See [Product - Attributes properties](#product-attributes-properties)                            |
| `default_attributes`    | array     | Defaults variation attributes. See [Product - Default attributes properties](#product-default-attributes-properties) |
| `variations`            | array     | List of variations IDs. <i class="label label-info">read-only</i>                                                    |
| `grouped_products`      | array     | List of grouped products ID.                                                                                         |
| `menu_order`            | integer   | Menu order, used to custom sort products.                                                                            |
| `meta_data`             | array     | Meta data. See [Product - Meta data properties](#product-meta-data-properties)                                       |

### Product - Downloads properties ###

| Attribute | Type   | Description |
|-----------|--------|-------------|
| `id`      | string | File ID.    |
| `name`    | string | File name.  |
| `file`    | string | File URL.   |

### Product - Dimensions properties ###

| Attribute | Type   | Description     |
|-----------|--------|-----------------|
| `length`  | string | Product length. |
| `width`   | string | Product width.  |
| `height`  | string | Product height. |

### Product - Categories properties ###

| Attribute | Type    | Description                                              |
|-----------|---------|----------------------------------------------------------|
| `id`      | integer | Category ID.                                             |
| `name`    | string  | Category name. <i class="label label-info">read-only</i> |
| `slug`    | string  | Category slug. <i class="label label-info">read-only</i> |

### Product - Tags properties ###

| Attribute | Type    | Description                                         |
|-----------|---------|-----------------------------------------------------|
| `id`      | integer | Tag ID.                                             |
| `name`    | string  | Tag name. <i class="label label-info">read-only</i> |
| `slug`    | string  | Tag slug. <i class="label label-info">read-only</i> |

### Product - Images properties ###

| Attribute           | Type      | Description                                                                                             |
|---------------------|-----------|---------------------------------------------------------------------------------------------------------|
| `id`                | integer   | The attachment ID from the Media Library.                                                               |
| `date_created`      | date-time | The date the image was created, in the site's timezone. <i class="label label-info">read-only</i>       |
| `date_created_gmt`  | date-time | The date the image was created, as GMT. <i class="label label-info">read-only</i>                       |
| `date_modified`     | date-time | The date the image was last modified, in the site's timezone. <i class="label label-info">read-only</i> |
| `date_modified_gmt` | date-time | The date the image was last modified, as GMT. <i class="label label-info">read-only</i>                 |
| `src`               | string    | Image URL.                                                                                              |
| `name`              | string    | Image name.                                                                                             |
| `alt`               | string    | Image alternative text.                                                                                 |

### Product - Attributes properties ###

| Attribute   | Type    | Description                                                                                                       |
|-------------|---------|-------------------------------------------------------------------------------------------------------------------|
| `id`        | integer | Attribute ID.                                                                                                     |
| `name`      | string  | Attribute name.                                                                                                   |
| `position`  | integer | Attribute position.                                                                                               |
| `visible`   | boolean | Define if the attribute is visible on the "Additional information" tab in the product's page. Default is `false`. |
| `variation` | boolean | Define if the attribute can be used as variation. Default is `false`.                                             |
| `options`   | array   | List of available term names of the attribute.                                                                    |

### Product - Default attributes properties ###

| Attribute | Type    | Description                   |
|-----------|---------|-------------------------------|
| `id`      | integer | Attribute ID.                 |
| `name`    | string  | Attribute name.               |
| `option`  | string  | Selected attribute term name. |

### Product - Meta data properties ###

| Attribute | Type    | Description                                        |
|-----------|---------|----------------------------------------------------|
| `id`      | integer | Meta ID. <i class="label label-info">read-only</i> |
| `key`     | string  | Meta key.                                          |
| `value`   | string  | Meta value.                                        |

## Create a product ##

This API helps you to create a new product.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-post">POST</i>
		<h6>/wp-json/wc/v3/products</h6>
	</div>
</div>

> Example of how to create a `simple` product with one existing image and one new image:

```shell
curl -X POST https://example.com/wp-json/wc/v3/products \
	-u consumer_key:consumer_secret \
	-H "Content-Type: application/json" \
	-d '{
  "name": "Premium Quality",
  "type": "simple",
  "regular_price": "21.99",
  "description": "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.",
  "short_description": "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.",
  "categories": [
    {
      "id": 9
    },
    {
      "id": 14
    }
  ],
  "images": [
    {
      "id": 42
    },
    {
      "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_back.jpg"
    }
  ]
}'
```

```javascript
const data = {
  name: "Premium Quality",
  type: "simple",
  regular_price: "21.99",
  description: "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.",
  short_description: "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.",
  categories: [
    {
      id: 9
    },
    {
      id: 14
    }
  ],
  images: [
    {
	  id: 42
    },
    {
      src: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_back.jpg"
    }
  ]
};

WooCommerce.post("products", data)
  .then((response) => {
    console.log(response.data);
  })
  .catch((error) => {
    console.log(error.response.data);
  });
```

```php
<?php
$data = [
    'name' => 'Premium Quality',
    'type' => 'simple',
    'regular_price' => '21.99',
    'description' => 'Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.',
    'short_description' => 'Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.',
    'categories' => [
        [
            'id' => 9
        ],
        [
            'id' => 14
        ]
    ],
    'images' => [
        [
            'id': 42
        ],
        [
            'src' => 'http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_back.jpg'
        ]
    ]
];

print_r($woocommerce->post('products', $data));
?>
```

```python
data = {
    "name": "Premium Quality",
    "type": "simple",
    "regular_price": "21.99",
    "description": "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.",
    "short_description": "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.",
    "categories": [
        {
            "id": 9
        },
        {
            "id": 14
        }
    ],
    "images": [
        {
            "id": 42
        },
        {
            "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_back.jpg"
        }
    ]
}

print(wcapi.post("products", data).json())
```

```ruby
data = {
  name: "Premium Quality",
  type: "simple",
  regular_price: "21.99",
  description: "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.",
  short_description: "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.",
  categories: [
    {
      id: 9
    },
    {
      id: 14
    }
  ],
  images: [
    {
      id: 42
    },
    {
      src: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_back.jpg",
    }
  ]
}

woocommerce.post("products", data).parsed_response
```

> JSON response example:

```json
{
  "id": 794,
  "name": "Premium Quality",
  "slug": "premium-quality-19",
  "permalink": "https://example.com/product/premium-quality-19/",
  "date_created": "2017-03-23T17:01:14",
  "date_created_gmt": "2017-03-23T20:01:14",
  "date_modified": "2017-03-23T17:01:14",
  "date_modified_gmt": "2017-03-23T20:01:14",
  "type": "simple",
  "status": "publish",
  "featured": false,
  "catalog_visibility": "visible",
  "description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>\n",
  "short_description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>\n",
  "sku": "",
  "price": "21.99",
  "regular_price": "21.99",
  "sale_price": "",
  "date_on_sale_from": null,
  "date_on_sale_from_gmt": null,
  "date_on_sale_to": null,
  "date_on_sale_to_gmt": null,
  "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>21.99</span>",
  "on_sale": false,
  "purchasable": true,
  "total_sales": 0,
  "virtual": false,
  "downloadable": false,
  "downloads": [],
  "download_limit": -1,
  "download_expiry": -1,
  "external_url": "",
  "button_text": "",
  "tax_status": "taxable",
  "tax_class": "",
  "manage_stock": false,
  "stock_quantity": null,
  "stock_status": "instock",
  "backorders": "no",
  "backorders_allowed": false,
  "backordered": false,
  "sold_individually": false,
  "weight": "",
  "dimensions": {
    "length": "",
    "width": "",
    "height": ""
  },
  "shipping_required": true,
  "shipping_taxable": true,
  "shipping_class": "",
  "shipping_class_id": 0,
  "reviews_allowed": true,
  "average_rating": "0.00",
  "rating_count": 0,
  "related_ids": [
    53,
    40,
    56,
    479,
    99
  ],
  "upsell_ids": [],
  "cross_sell_ids": [],
  "parent_id": 0,
  "purchase_note": "",
  "categories": [
    {
      "id": 9,
      "name": "Clothing",
      "slug": "clothing"
    },
    {
      "id": 14,
      "name": "T-shirts",
      "slug": "t-shirts"
    }
  ],
  "tags": [],
  "images": [
    {
      "id": 42,
      "date_created": "2017-03-22T14:01:13",
      "date_created_gmt": "2017-03-22T20:01:13",
      "date_modified": "2017-03-22T14:01:13",
      "date_modified_gmt": "2017-03-22T20:01:13",
      "src": "https://example.com/wp-content/uploads/2017/03/T_2_front-4.jpg",
      "name": "",
      "alt": ""
    },
    {
      "id": 793,
      "date_created": "2017-03-23T14:01:14",
      "date_created_gmt": "2017-03-23T20:01:14",
      "date_modified": "2017-03-23T14:01:14",
      "date_modified_gmt": "2017-03-23T20:01:14",
      "src": "https://example.com/wp-content/uploads/2017/03/T_2_back-2.jpg",
      "name": "",
      "alt": ""
    }
  ],
  "attributes": [],
  "default_attributes": [],
  "variations": [],
  "grouped_products": [],
  "menu_order": 0,
  "meta_data": [],
  "_links": {
    "self": [
      {
        "href": "https://example.com/wp-json/wc/v3/products/794"
      }
    ],
    "collection": [
      {
        "href": "https://example.com/wp-json/wc/v3/products"
      }
    ]
  }
}
```

> Example of how to create a `variable` product with global and non-global attributes:

```shell
curl -X POST https://example.com/wp-json/wc/v3/products \
	-u consumer_key:consumer_secret \
	-H "Content-Type: application/json" \
	-d '{
  "name": "Ship Your Idea",
  "type": "variable",
  "description": "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.",
  "short_description": "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.",
  "categories": [
    {
      "id": 9
    },
    {
      "id": 14
    }
  ],
  "images": [
    {
      "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_4_front.jpg"
    },
    {
      "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_4_back.jpg"
    },
    {
      "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_3_front.jpg"
    },
    {
      "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_3_back.jpg"
    }
  ],
  "attributes": [
    {
      "id": 6,
      "position": 0,
      "visible": false,
      "variation": true,
      "options": [
        "Black",
        "Green"
      ]
    },
    {
      "name": "Size",
      "position": 0,
      "visible": true,
      "variation": true,
      "options": [
        "S",
        "M"
      ]
    }
  ],
  "default_attributes": [
    {
      "id": 6,
      "option": "Black"
    },
    {
      "name": "Size",
      "option": "S"
    }
  ]
}'
```

```javascript
const data = {
  name: "Ship Your Idea",
  type: "variable",
  description: "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.",
  short_description: "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.",
  categories: [
    {
      id: 9
    },
    {
      id: 14
    }
  ],
  images: [
    {
      src: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_4_front.jpg"
    },
    {
      src: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_4_back.jpg"
    },
    {
      src: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_3_front.jpg"
    },
    {
      src: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_3_back.jpg"
    }
  ],
  attributes: [
    {
      id: 6,
      position: 0,
      visible: true,
      variation: true,
      options: [
        "Black",
        "Green"
      ]
    },
    {
      name: "Size",
      position: 0,
      visible: false,
      variation: true,
      options: [
        "S",
        "M"
      ]
    }
  ],
  default_attributes: [
    {
      id: 6,
      option: "Black"
    },
    {
      name: "Size",
      option: "S"
    }
  ]
};

WooCommerce.post("products", data)
  .then((response) => {
    console.log(response.data);
  })
  .catch((error) => {
    console.log(error.response.data);
  });
```

```php
<?php
$data = [
    'name' => 'Ship Your Idea',
    'type' => 'variable',
    'description' => 'Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.',
    'short_description' => 'Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.',
    'categories' => [
        [
            'id' => 9
        ],
        [
            'id' => 14
        ]
    ],
    'images' => [
        [
            'src' => 'http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_4_front.jpg'
        ],
        [
            'src' => 'http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_4_back.jpg'
        ],
        [
            'src' => 'http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_3_front.jpg'
        ],
        [
            'src' => 'http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_3_back.jpg'
        ]
    ],
    'attributes' => [
        [
            'id' => 6,
            'position' => 0,
            'visible' => false,
            'variation' => true,
            'options' => [
                'Black',
                'Green'
            ]
        ],
        [
            'name' => 'Size',
            'position' => 0,
            'visible' => true,
            'variation' => true,
            'options' => [
                'S',
                'M'
            ]
        ]
    ],
    'default_attributes' => [
        [
            'id' => 6,
            'option' => 'Black'
        ],
        [
            'name' => 'Size',
            'option' => 'S'
        ]
    ]
];

print_r($woocommerce->post('products', $data));
?>
```

```python
data = {
    "name": "Ship Your Idea",
    "type": "variable",
    "description": "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.",
    "short_description": "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.",
    "categories": [
        {
            "id": 9
        },
        {
            "id": 14
        }
    ],
    "images": [
        {
            "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_4_front.jpg"
        },
        {
            "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_4_back.jpg"
        },
        {
            "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_3_front.jpg"
        },
        {
            "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_3_back.jpg"
        }
    ],
    "attributes": [
        {
            "id": 6,
            "position": 0,
            "visible": False,
            "variation": True,
            "options": [
                "Black",
                "Green"
            ]
        },
        {
            "name": "Size",
            "position": 0,
            "visible": True,
            "variation": True,
            "options": [
                "S",
                "M"
            ]
        }
    ],
    "default_attributes": [
        {
            "id": 6,
            "option": "Black"
        },
        {
            "name": "Size",
            "option": "S"
        }
    ]
}

print(wcapi.post("products", data).json())
```

```ruby
data = {
  name: "Ship Your Idea",
  type: "variable",
  description: "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.",
  short_description: "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.",
  categories: [
    {
      id: 9
    },
    {
      id: 14
    }
  ],
  images: [
    {
      src: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_4_front.jpg"
    },
    {
      src: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_4_back.jpg"
    },
    {
      src: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_3_front.jpg"
    },
    {
      src: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_3_back.jpg"
    }
  ],
  attributes: [
    {
      id: 6,
      position: 0,
      visible: false,
      variation: true,
      options: [
        "Black",
        "Green"
      ]
    },
    {
      name: "Size",
      position: 0,
      visible: true,
      variation: true,
      options: [
        "S",
        "M"
      ]
    }
  ],
  default_attributes: [
    {
      id: 6,
      option: "Black"
    },
    {
      name: "Size",
      option: "S"
    }
  ]
}

woocommerce.post("products", data).parsed_response
```

> JSON response example:

```json
{
  "id": 799,
  "name": "Ship Your Idea",
  "slug": "ship-your-idea-22",
  "permalink": "https://example.com/product/ship-your-idea-22/",
  "date_created": "2017-03-23T17:03:12",
  "date_created_gmt": "2017-03-23T20:03:12",
  "date_modified": "2017-03-23T17:03:12",
  "date_modified_gmt": "2017-03-23T20:03:12",
  "type": "variable",
  "status": "publish",
  "featured": false,
  "catalog_visibility": "visible",
  "description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>\n",
  "short_description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>\n",
  "sku": "",
  "price": "",
  "regular_price": "",
  "sale_price": "",
  "date_on_sale_from": null,
  "date_on_sale_from_gmt": null,
  "date_on_sale_to": null,
  "date_on_sale_to_gmt": null,
  "price_html": "",
  "on_sale": false,
  "purchasable": false,
  "total_sales": 0,
  "virtual": false,
  "downloadable": false,
  "downloads": [],
  "download_limit": -1,
  "download_expiry": -1,
  "external_url": "",
  "button_text": "",
  "tax_status": "taxable",
  "tax_class": "",
  "manage_stock": false,
  "stock_quantity": null,
  "stock_status": "instock",
  "backorders": "no",
  "backorders_allowed": false,
  "backordered": false,
  "sold_individually": false,
  "weight": "",
  "dimensions": {
    "length": "",
    "width": "",
    "height": ""
  },
  "shipping_required": true,
  "shipping_taxable": true,
  "shipping_class": "",
  "shipping_class_id": 0,
  "reviews_allowed": true,
  "average_rating": "0.00",
  "rating_count": 0,
  "related_ids": [
    472,
    387,
    19,
    53,
    396
  ],
  "upsell_ids": [],
  "cross_sell_ids": [],
  "parent_id": 0,
  "purchase_note": "",
  "categories": [
    {
      "id": 9,
      "name": "Clothing",
      "slug": "clothing"
    },
    {
      "id": 14,
      "name": "T-shirts",
      "slug": "t-shirts"
    }
  ],
  "tags": [],
  "images": [
    {
      "id": 795,
      "date_created": "2017-03-23T14:03:08",
      "date_created_gmt": "2017-03-23T20:03:08",
      "date_modified": "2017-03-23T14:03:08",
      "date_modified_gmt": "2017-03-23T20:03:08",
      "src": "https://example.com/wp-content/uploads/2017/03/T_4_front-11.jpg",
      "name": "",
      "alt": ""
    },
    {
      "id": 796,
      "date_created": "2017-03-23T14:03:09",
      "date_created_gmt": "2017-03-23T20:03:09",
      "date_modified": "2017-03-23T14:03:09",
      "date_modified_gmt": "2017-03-23T20:03:09",
      "src": "https://example.com/wp-content/uploads/2017/03/T_4_back-10.jpg",
      "name": "",
      "alt": ""
    },
    {
      "id": 797,
      "date_created": "2017-03-23T14:03:10",
      "date_created_gmt": "2017-03-23T20:03:10",
      "date_modified": "2017-03-23T14:03:10",
      "date_modified_gmt": "2017-03-23T20:03:10",
      "src": "https://example.com/wp-content/uploads/2017/03/T_3_front-10.jpg",
      "name": "",
      "alt": ""
    },
    {
      "id": 798,
      "date_created": "2017-03-23T14:03:11",
      "date_created_gmt": "2017-03-23T20:03:11",
      "date_modified": "2017-03-23T14:03:11",
      "date_modified_gmt": "2017-03-23T20:03:11",
      "src": "https://example.com/wp-content/uploads/2017/03/T_3_back-10.jpg",
      "name": "",
      "alt": ""
    }
  ],
  "attributes": [
    {
      "id": 6,
      "name": "Color",
      "position": 0,
      "visible": false,
      "variation": true,
      "options": [
        "Black",
        "Green"
      ]
    },
    {
      "id": 0,
      "name": "Size",
      "position": 0,
      "visible": true,
      "variation": true,
      "options": [
        "S",
        "M"
      ]
    }
  ],
  "default_attributes": [
    {
      "id": 6,
      "name": "Color",
      "option": "black"
    },
    {
      "id": 0,
      "name": "Size",
      "option": "S"
    }
  ],
  "variations": [],
  "grouped_products": [],
  "menu_order": 0,
  "meta_data": [],
  "_links": {
    "self": [
      {
        "href": "https://example.com/wp-json/wc/v3/products/799"
      }
    ],
    "collection": [
      {
        "href": "https://example.com/wp-json/wc/v3/products"
      }
    ]
  }
}
```

## Retrieve a product ##

This API lets you retrieve and view a specific product by ID.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/wc/v3/products/&lt;id&gt;</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/wc/v3/products/794 \
	-u consumer_key:consumer_secret
```

```javascript
WooCommerce.get("products/794")
  .then((response) => {
    console.log(response.data);
  })
  .catch((error) => {
    console.log(error.response.data);
  });
```

```php
<?php print_r($woocommerce->get('products/794')); ?>
```

```python
print(wcapi.get("products/794").json())
```

```ruby
woocommerce.get("products/794").parsed_response
```

> JSON response example:

```json
{
  "id": 794,
  "name": "Premium Quality",
  "slug": "premium-quality-19",
  "permalink": "https://example.com/product/premium-quality-19/",
  "date_created": "2017-03-23T17:01:14",
  "date_created_gmt": "2017-03-23T20:01:14",
  "date_modified": "2017-03-23T17:01:14",
  "date_modified_gmt": "2017-03-23T20:01:14",
  "type": "simple",
  "status": "publish",
  "featured": false,
  "catalog_visibility": "visible",
  "description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>\n",
  "short_description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>\n",
  "sku": "",
  "price": "21.99",
  "regular_price": "21.99",
  "sale_price": "",
  "date_on_sale_from": null,
  "date_on_sale_from_gmt": null,
  "date_on_sale_to": null,
  "date_on_sale_to_gmt": null,
  "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>21.99</span>",
  "on_sale": false,
  "purchasable": true,
  "total_sales": 0,
  "virtual": false,
  "downloadable": false,
  "downloads": [],
  "download_limit": -1,
  "download_expiry": -1,
  "external_url": "",
  "button_text": "",
  "tax_status": "taxable",
  "tax_class": "",
  "manage_stock": false,
  "stock_quantity": null,
  "stock_status": "instock",
  "backorders": "no",
  "backorders_allowed": false,
  "backordered": false,
  "sold_individually": false,
  "weight": "",
  "dimensions": {
    "length": "",
    "width": "",
    "height": ""
  },
  "shipping_required": true,
  "shipping_taxable": true,
  "shipping_class": "",
  "shipping_class_id": 0,
  "reviews_allowed": true,
  "average_rating": "0.00",
  "rating_count": 0,
  "related_ids": [
    53,
    40,
    56,
    479,
    99
  ],
  "upsell_ids": [],
  "cross_sell_ids": [],
  "parent_id": 0,
  "purchase_note": "",
  "categories": [
    {
      "id": 9,
      "name": "Clothing",
      "slug": "clothing"
    },
    {
      "id": 14,
      "name": "T-shirts",
      "slug": "t-shirts"
    }
  ],
  "tags": [],
  "images": [
    {
      "id": 792,
      "date_created": "2017-03-23T14:01:13",
      "date_created_gmt": "2017-03-23T20:01:13",
      "date_modified": "2017-03-23T14:01:13",
      "date_modified_gmt": "2017-03-23T20:01:13",
      "src": "https://example.com/wp-content/uploads/2017/03/T_2_front-4.jpg",
      "name": "",
      "alt": ""
    },
    {
      "id": 793,
      "date_created": "2017-03-23T14:01:14",
      "date_created_gmt": "2017-03-23T20:01:14",
      "date_modified": "2017-03-23T14:01:14",
      "date_modified_gmt": "2017-03-23T20:01:14",
      "src": "https://example.com/wp-content/uploads/2017/03/T_2_back-2.jpg",
      "name": "",
      "alt": ""
    }
  ],
  "attributes": [],
  "default_attributes": [],
  "variations": [],
  "grouped_products": [],
  "menu_order": 0,
  "meta_data": [],
  "_links": {
    "self": [
      {
        "href": "https://example.com/wp-json/wc/v3/products/794"
      }
    ],
    "collection": [
      {
        "href": "https://example.com/wp-json/wc/v3/products"
      }
    ]
  }
}
```

## List all products ##

This API helps you to view all the products.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json/wc/v3/products</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/wc/v3/products \
	-u consumer_key:consumer_secret
```

```javascript
WooCommerce.get("products")
  .then((response) => {
    console.log(response.data);
  })
  .catch((error) => {
    console.log(error.response.data);
  });
```

```php
<?php print_r($woocommerce->get('products')); ?>
```

```python
print(wcapi.get("products").json())
```

```ruby
woocommerce.get("products").parsed_response
```

> JSON response example:

```json
[
  {
    "id": 799,
    "name": "Ship Your Idea",
    "slug": "ship-your-idea-22",
    "permalink": "https://example.com/product/ship-your-idea-22/",
    "date_created": "2017-03-23T17:03:12",
    "date_created_gmt": "2017-03-23T20:03:12",
    "date_modified": "2017-03-23T17:03:12",
    "date_modified_gmt": "2017-03-23T20:03:12",
    "type": "variable",
    "status": "publish",
    "featured": false,
    "catalog_visibility": "visible",
    "description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>\n",
    "short_description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>\n",
    "sku": "",
    "price": "",
    "regular_price": "",
    "sale_price": "",
    "date_on_sale_from": null,
    "date_on_sale_from_gmt": null,
    "date_on_sale_to": null,
    "date_on_sale_to_gmt": null,
    "price_html": "",
    "on_sale": false,
    "purchasable": false,
    "total_sales": 0,
    "virtual": false,
    "downloadable": false,
    "downloads": [],
    "download_limit": -1,
    "download_expiry": -1,
    "external_url": "",
    "button_text": "",
    "tax_status": "taxable",
    "tax_class": "",
    "manage_stock": false,
    "stock_quantity": null,
    "stock_status": "instock",
    "backorders": "no",
    "backorders_allowed": false,
    "backordered": false,
    "sold_individually": false,
    "weight": "",
    "dimensions": {
      "length": "",
      "width": "",
      "height": ""
    },
    "shipping_required": true,
    "shipping_taxable": true,
    "shipping_class": "",
    "shipping_class_id": 0,
    "reviews_allowed": true,
    "average_rating": "0.00",
    "rating_count": 0,
    "related_ids": [
      31,
      22,
      369,
      414,
      56
    ],
    "upsell_ids": [],
    "cross_sell_ids": [],
    "parent_id": 0,
    "purchase_note": "",
    "categories": [
      {
        "id": 9,
        "name": "Clothing",
        "slug": "clothing"
      },
      {
        "id": 14,
        "name": "T-shirts",
        "slug": "t-shirts"
      }
    ],
    "tags": [],
    "images": [
      {
        "id": 795,
        "date_created": "2017-03-23T14:03:08",
        "date_created_gmt": "2017-03-23T20:03:08",
        "date_modified": "2017-03-23T14:03:08",
        "date_modified_gmt": "2017-03-23T20:03:08",
        "src": "https://example.com/wp-content/uploads/2017/03/T_4_front-11.jpg",
        "name": "",
        "alt": ""
      },
      {
        "id": 796,
        "date_created": "2017-03-23T14:03:09",
        "date_created_gmt": "2017-03-23T20:03:09",
        "date_modified": "2017-03-23T14:03:09",
        "date_modified_gmt": "2017-03-23T20:03:09",
        "src": "https://example.com/wp-content/uploads/2017/03/T_4_back-10.jpg",
        "name": "",
        "alt": ""
      },
      {
        "id": 797,
        "date_created": "2017-03-23T14:03:10",
        "date_created_gmt": "2017-03-23T20:03:10",
        "date_modified": "2017-03-23T14:03:10",
        "date_modified_gmt": "2017-03-23T20:03:10",
        "src": "https://example.com/wp-content/uploads/2017/03/T_3_front-10.jpg",
        "name": "",
        "alt": ""
      },
      {
        "id": 798,
        "date_created": "2017-03-23T14:03:11",
        "date_created_gmt": "2017-03-23T20:03:11",
        "date_modified": "2017-03-23T14:03:11",
        "date_modified_gmt": "2017-03-23T20:03:11",
        "src": "https://example.com/wp-content/uploads/2017/03/T_3_back-10.jpg",
        "name": "",
        "alt": ""
      }
    ],
    "attributes": [
      {
        "id": 6,
        "name": "Color",
        "position": 0,
        "visible": false,
        "variation": true,
        "options": [
          "Black",
          "Green"
        ]
      },
      {
        "id": 0,
        "name": "Size",
        "position": 0,
        "visible": true,
        "variation": true,
        "options": [
          "S",
          "M"
        ]
      }
    ],
    "default_attributes": [],
    "variations": [],
    "grouped_products": [],
    "menu_order": 0,
    "meta_data": [],
    "_links": {
      "self": [
        {
          "href": "https://example.com/wp-json/wc/v3/products/799"
        }
      ],
      "collection": [
        {
          "href": "https://example.com/wp-json/wc/v3/products"
        }
      ]
    }
  },
  {
    "id": 794,
    "name": "Premium Quality",
    "slug": "premium-quality-19",
    "permalink": "https://example.com/product/premium-quality-19/",
    "date_created": "2017-03-23T17:01:14",
    "date_created_gmt": "2017-03-23T20:01:14",
    "date_modified": "2017-03-23T17:01:14",
    "date_modified_gmt": "2017-03-23T20:01:14",
    "type": "simple",
    "status": "publish",
    "featured": false,
    "catalog_visibility": "visible",
    "description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>\n",
    "short_description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>\n",
    "sku": "",
    "price": "21.99",
    "regular_price": "21.99",
    "sale_price": "",
    "date_on_sale_from": null,
    "date_on_sale_from_gmt": null,
    "date_on_sale_to": null,
    "date_on_sale_to_gmt": null,
    "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>21.99</span>",
    "on_sale": false,
    "purchasable": true,
    "total_sales": 0,
    "virtual": false,
    "downloadable": false,
    "downloads": [],
    "download_limit": -1,
    "download_expiry": -1,
    "external_url": "",
    "button_text": "",
    "tax_status": "taxable",
    "tax_class": "",
    "manage_stock": false,
    "stock_quantity": null,
    "stock_status": "instock",
    "backorders": "no",
    "backorders_allowed": false,
    "backordered": false,
    "sold_individually": false,
    "weight": "",
    "dimensions": {
      "length": "",
      "width": "",
      "height": ""
    },
    "shipping_required": true,
    "shipping_taxable": true,
    "shipping_class": "",
    "shipping_class_id": 0,
    "reviews_allowed": true,
    "average_rating": "0.00",
    "rating_count": 0,
    "related_ids": [
      463,
      47,
      31,
      387,
      458
    ],
    "upsell_ids": [],
    "cross_sell_ids": [],
    "parent_id": 0,
    "purchase_note": "",
    "categories": [
      {
        "id": 9,
        "name": "Clothing",
        "slug": "clothing"
      },
      {
        "id": 14,
        "name": "T-shirts",
        "slug": "t-shirts"
      }
    ],
    "tags": [],
    "images": [
      {
        "id": 792,
        "date_created": "2017-03-23T14:01:13",
        "date_created_gmt": "2017-03-23T20:01:13",
        "date_modified": "2017-03-23T14:01:13",
        "date_modified_gmt": "2017-03-23T20:01:13",
        "src": "https://example.com/wp-content/uploads/2017/03/T_2_front-4.jpg",
        "name": "",
        "alt": ""
      },
      {
        "id": 793,
        "date_created": "2017-03-23T14:01:14",
        "date_created_gmt": "2017-03-23T20:01:14",
        "date_modified": "2017-03-23T14:01:14",
        "date_modified_gmt": "2017-03-23T20:01:14",
        "src": "https://example.com/wp-content/uploads/2017/03/T_2_back-2.jpg",
        "name": "",
        "alt": ""
      }
    ],
    "attributes": [],
    "default_attributes": [
      {
        "id": 6,
        "name": "Color",
        "option": "black"
      },
      {
        "id": 0,
        "name": "Size",
        "option": "S"
      }
    ],
    "variations": [],
    "grouped_products": [],
    "menu_order": 0,
    "meta_data": [],
    "_links": {
      "self": [
        {
          "href": "https://example.com/wp-json/wc/v3/products/794"
        }
      ],
      "collection": [
        {
          "href": "https://example.com/wp-json/wc/v3/products"
        }
      ]
    }
  }
]
```

#### Available parameters ####

| Parameter         | Type    | Description                                                                                                                                                               |
|-------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context`         | string  | Scope under which the request is made; determines fields present in response. Options: `view` and `edit`. Default is `view`.                                              |
| `page`            | integer | Current page of the collection. Default is `1`.                                                                                                                           |
| `per_page`        | integer | Maximum number of items to be returned in result set. Default is `10`.                                                                                                    |
| `search`          | string  | Limit results to those matching a string.                                                                                                                                 |
| `after`           | string  | Limit response to resources published after a given ISO8601 compliant date.                                                                                               |
| `before`          | string  | Limit response to resources published before a given ISO8601 compliant date.                                                                                              |
| `modified_after`  | string  | Limit response to resources modified after a given ISO8601 compliant date.                                                                                                |
| `modified_before` | string  | Limit response to resources modified after a given ISO8601 compliant date.                                                                                                |
| `dates_are_gmt`   | boolean | Whether to consider GMT post dates when limiting response by published or modified date.                                                                                  |
| `exclude`         | array   | Ensure result set excludes specific IDs.                                                                                                                                  |
| `include`         | array   | Limit result set to specific ids.                                                                                                                                         |
| `offset`          | integer | Offset the result set by a specific number of items.                                                                                                                      |
| `order`           | string  | Order sort attribute ascending or descending. Options: `asc` and `desc`. Default is `desc`.                                                                               |
| `orderby`         | string  | Sort collection by object attribute. Options: `date`, `modified`, `id`, `include`, `title`, `slug`, `price`, `popularity`, `rating`, and `menu_order`. Default is `date`. |
| `parent`          | array   | Limit result set to those of particular parent IDs.                                                                                                                       |
| `parent_exclude`  | array   | Limit result set to all items except those of a particular parent ID.                                                                                                     |
| `slug`            | string  | Limit result set to products with a specific slug.                                                                                                                        |
| `status`          | string  | Limit result set to products assigned a specific status. Options: `any`, `draft`, `pending`, `private` and `publish`. Default is `any`.                                   |
| `type`            | string  | Limit result set to products assigned a specific type. Options: `simple`, `grouped`, `external` and `variable`.                                                           |
| `sku`             | string  | Limit result set to products with a specific SKU.                                                                                                                         |
| `featured`        | boolean | Limit result set to featured products.                                                                                                                                    |
| `category`        | string  | Limit result set to products assigned a specific category ID.                                                                                                             |
| `tag`             | string  | Limit result set to products assigned a specific tag ID.                                                                                                                  |
| `shipping_class`  | string  | Limit result set to products assigned a specific shipping class ID.                                                                                                       |
| `attribute`       | string  | Limit result set to products with a specific attribute.                                                                                                                   |
| `attribute_term`  | string  | Limit result set to products with a specific attribute term ID (required an assigned attribute).                                                                          |
| `tax_class`       | string  | Limit result set to products with a specific tax class. Default options: `standard`, `reduced-rate` and `zero-rate`.                                                      |
| `on_sale`         | boolean | Limit result set to products on sale.                                                                                                                                     |
| `min_price`       | string  | Limit result set to products based on a minimum price.                                                                                                                    |
| `max_price`       | string  | Limit result set to products based on a maximum price.                                                                                                                    |
| `stock_status`    | string  | Limit result set to products with specified stock status. Options: `instock`, `outofstock` and `onbackorder`.                                                             |

## Duplicate product ##

This API helps you to duplicate a product.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-post">POST</i>
		<h6>/wp-json/wc/v3/products/&lt;product_id&gt;/duplicate</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/wc/v3/products/<product_id>/duplicate \
	-u consumer_key:consumer_secret
```

```javascript
WooCommerce.post("products/2/duplicate")
  .then((response) => {
    console.log(response.data);
  })
  .catch((error) => {
    console.log(error.response.data);
  });
```

```php
<?php print_r($woocommerce->post('products/2/duplicate')); ?>
```

```python
print(wcapi.post("products/2/duplicate").json())
```

```ruby
woocommerce.post("products/2/duplicate").parsed_response
```

> JSON response example:

```json
{
  "id": 824,
  "name": "Premium Quality (Copy)",
  "slug": "",
  "date_created": {
    "date": "2024-05-30 19:16:39.000000",
    "timezone_type": 1,
    "timezone": "+00:00"
  },
  "date_modified": {
    "date": "2024-03-08 15:03:19.000000",
    "timezone_type": 1,
    "timezone": "+00:00"
  },
  "status": "draft",
  "featured": false,
  "catalog_visibility": "visible",
  "description": "",
  "short_description": "",
  "sku": "product-22-1",
  "price": "",
  "regular_price": "",
  "sale_price": "",
  "date_on_sale_from": null,
  "date_on_sale_to": null,
  "total_sales": 0,
  "tax_status": "taxable",
  "tax_class": "",
  "manage_stock": false,
  "stock_quantity": null,
  "stock_status": "instock",
  "backorders": "no",
  "low_stock_amount": "",
  "sold_individually": false,
  "weight": "",
  "length": "",
  "width": "",
  "height": "",
  "upsell_ids": [],
  "cross_sell_ids": [],
  "parent_id": 0,
  "reviews_allowed": true,
  "purchase_note": "",
  "attributes": [],
  "default_attributes": [],
  "menu_order": 0,
  "post_password": "",
  "virtual": false,
  "downloadable": false,
  "category_ids": [
    15
  ],
  "tag_ids": [],
  "shipping_class_id": 0,
  "downloads": [],
  "image_id": "",
  "gallery_image_ids": [],
  "download_limit": -1,
  "download_expiry": -1,
  "rating_counts": [],
  "average_rating": "0",
  "review_count": 0,
  "meta_data": []
}
```

## Update a product ##

This API lets you make changes to a product.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-put">PUT</i>
		<h6>/wp-json/wc/v3/products/&lt;id&gt;</h6>
	</div>
</div>

```shell
curl -X PUT https://example.com/wp-json/wc/v3/products/794 \
	-u consumer_key:consumer_secret \
	-H "Content-Type: application/json" \
	-d '{
  "regular_price": "24.54"
}'
```

```javascript
const data = {
  regular_price: "24.54"
};

WooCommerce.put("products/794", data)
  .then((response) => {
    console.log(response.data);
  })
  .catch((error) => {
    console.log(error.response.data);
  });
```

```php
<?php
$data = [
    'regular_price' => '24.54'
];

print_r($woocommerce->put('products/794', $data));
?>
```

```python
data = {
    "regular_price": "24.54"
}

print(wcapi.put("products/794", data).json())
```

```ruby
data = {
  regular_price: "24.54"
}

woocommerce.put("products/794", data).parsed_response
```

> JSON response example:

```json
{
  "id": 794,
  "name": "Premium Quality",
  "slug": "premium-quality-19",
  "permalink": "https://example.com/product/premium-quality-19/",
  "date_created": "2017-03-23T17:01:14",
  "date_created_gmt": "2017-03-23T20:01:14",
  "date_modified": "2017-03-23T17:01:14",
  "date_modified_gmt": "2017-03-23T20:01:14",
  "type": "simple",
  "status": "publish",
  "featured": false,
  "catalog_visibility": "visible",
  "description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>\n",
  "short_description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>\n",
  "sku": "",
  "price": "24.54",
  "regular_price": "24.54",
  "sale_price": "",
  "date_on_sale_from": null,
  "date_on_sale_from_gmt": null,
  "date_on_sale_to": null,
  "date_on_sale_to_gmt": null,
  "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>24.54</span>",
  "on_sale": false,
  "purchasable": true,
  "total_sales": 0,
  "virtual": false,
  "downloadable": false,
  "downloads": [],
  "download_limit": -1,
  "download_expiry": -1,
  "external_url": "",
  "button_text": "",
  "tax_status": "taxable",
  "tax_class": "",
  "manage_stock": false,
  "stock_quantity": null,
  "stock_status": "instock",
  "backorders": "no",
  "backorders_allowed": false,
  "backordered": false,
  "sold_individually": false,
  "weight": "",
  "dimensions": {
    "length": "",
    "width": "",
    "height": ""
  },
  "shipping_required": true,
  "shipping_taxable": true,
  "shipping_class": "",
  "shipping_class_id": 0,
  "reviews_allowed": true,
  "average_rating": "0.00",
  "rating_count": 0,
  "related_ids": [
    479,
    387,
    22,
    463,
    396
  ],
  "upsell_ids": [],
  "cross_sell_ids": [],
  "parent_id": 0,
  "purchase_note": "",
  "categories": [
    {
      "id": 9,
      "name": "Clothing",
      "slug": "clothing"
    },
    {
      "id": 14,
      "name": "T-shirts",
      "slug": "t-shirts"
    }
  ],
  "tags": [],
  "images": [
    {
      "id": 792,
      "date_created": "2017-03-23T14:01:13",
      "date_created_gmt": "2017-03-23T20:01:13",
      "date_modified": "2017-03-23T14:01:13",
      "date_modified_gmt": "2017-03-23T20:01:13",
      "src": "https://example.com/wp-content/uploads/2017/03/T_2_front-4.jpg",
      "name": "",
      "alt": ""
    },
    {
      "id": 793,
      "date_created": "2017-03-23T14:01:14",
      "date_created_gmt": "2017-03-23T20:01:14",
      "date_modified": "2017-03-23T14:01:14",
      "date_modified_gmt": "2017-03-23T20:01:14",
      "src": "https://example.com/wp-content/uploads/2017/03/T_2_back-2.jpg",
      "name": "",
      "alt": ""
    }
  ],
  "attributes": [],
  "default_attributes": [],
  "variations": [],
  "grouped_products": [],
  "menu_order": 0,
  "meta_data": [],
  "_links": {
    "self": [
      {
        "href": "https://example.com/wp-json/wc/v3/products/794"
      }
    ],
    "collection": [
      {
        "href": "https://example.com/wp-json/wc/v3/products"
      }
    ]
  }
}
```

## Delete a product ##

This API helps you delete a product.

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-delete">DELETE</i>
		<h6>/wp-json/wc/v3/products/&lt;id&gt;</h6>
	</div>
</div>

```shell
curl -X DELETE https://example.com/wp-json/wc/v3/products/794?force=true \
	-u consumer_key:consumer_secret
```

```javascript
WooCommerce.delete("products/794", {
  force: true
})
  .then((response) => {
    console.log(response.data);
  })
  .catch((error) => {
    console.log(error.response.data);
  });
```

```php
<?php print_r($woocommerce->delete('products/794', ['force' => true])); ?>
```

```python
print(wcapi.delete("products/794", params={"force": True}).json())
```

```ruby
woocommerce.delete("products/794", force: true).parsed_response
```

> JSON response example:

```json
{
  "id": 794,
  "name": "Premium Quality",
  "slug": "premium-quality-19",
  "permalink": "https://example.com/product/premium-quality-19/",
  "date_created": "2017-03-23T17:01:14",
  "date_created_gmt": "2017-03-23T20:01:14",
  "date_modified": "2017-03-23T17:01:14",
  "date_modified_gmt": "2017-03-23T20:01:14",
  "type": "simple",
  "status": "publish",
  "featured": false,
  "catalog_visibility": "visible",
  "description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>\n",
  "short_description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>\n",
  "sku": "",
  "price": "24.54",
  "regular_price": "24.54",
  "sale_price": "",
  "date_on_sale_from": null,
  "date_on_sale_from_gmt": null,
  "date_on_sale_to": null,
  "date_on_sale_to_gmt": null,
  "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>24.54</span>",
  "on_sale": false,
  "purchasable": true,
  "total_sales": 0,
  "virtual": false,
  "downloadable": false,
  "downloads": [],
  "download_limit": -1,
  "download_expiry": -1,
  "external_url": "",
  "button_text": "",
  "tax_status": "taxable",
  "tax_class": "",
  "manage_stock": false,
  "stock_quantity": null,
  "stock_status": "instock",
  "backorders": "no",
  "backorders_allowed": false,
  "backordered": false,
  "sold_individually": false,
  "weight": "",
  "dimensions": {
    "length": "",
    "width": "",
    "height": ""
  },
  "shipping_required": true,
  "shipping_taxable": true,
  "shipping_class": "",
  "shipping_class_id": 0,
  "reviews_allowed": true,
  "average_rating": "0.00",
  "rating_count": 0,
  "related_ids": [
    479,
    387,
    22,
    463,
    396
  ],
  "upsell_ids": [],
  "cross_sell_ids": [],
  "parent_id": 0,
  "purchase_note": "",
  "categories": [
    {
      "id": 9,
      "name": "Clothing",
      "slug": "clothing"
    },
    {
      "id": 14,
      "name": "T-shirts",
      "slug": "t-shirts"
    }
  ],
  "tags": [],
  "images": [
    {
      "id": 792,
      "date_created": "2017-03-23T14:01:13",
      "date_created_gmt": "2017-03-23T20:01:13",
      "date_modified": "2017-03-23T14:01:13",
      "date_modified_gmt": "2017-03-23T20:01:13",
      "src": "https://example.com/wp-content/uploads/2017/03/T_2_front-4.jpg",
      "name": "",
      "alt": ""
    },
    {
      "id": 793,
      "date_created": "2017-03-23T14:01:14",
      "date_created_gmt": "2017-03-23T20:01:14",
      "date_modified": "2017-03-23T14:01:14",
      "date_modified_gmt": "2017-03-23T20:01:14",
      "src": "https://example.com/wp-content/uploads/2017/03/T_2_back-2.jpg",
      "name": "",
      "alt": ""
    }
  ],
  "attributes": [],
  "default_attributes": [],
  "variations": [],
  "grouped_products": [],
  "menu_order": 0,
  "meta_data": [],
  "_links": {
    "self": [
      {
        "href": "https://example.com/wp-json/wc/v3/products/794"
      }
    ],
    "collection": [
      {
        "href": "https://example.com/wp-json/wc/v3/products"
      }
    ]
  }
}
```

#### Available parameters ####

| Parameter | Type   | Description                                                               |
|-----------|--------|---------------------------------------------------------------------------|
| `force`   | string | Use `true` whether to permanently delete the product, Default is `false`. |

## Batch update products ##

This API helps you to batch create, update and delete multiple products.

<aside class="notice">
Note: By default it's limited to up to 100 objects to be created, updated or deleted. 
</aside>

### HTTP request ###

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-post">POST</i>
		<h6>/wp-json/wc/v3/products/batch</h6>
	</div>
</div>

```shell
curl -X POST https://example.com/wp-json/wc/v3/products/batch \
	-u consumer_key:consumer_secret \
	-H "Content-Type: application/json" \
	-d '{
  "create": [
    {
      "name": "Woo Single #1",
      "type": "simple",
      "regular_price": "21.99",
      "virtual": true,
      "downloadable": true,
      "downloads": [
        {
          "name": "Woo Single",
          "file": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/cd_4_angle.jpg"
        }
      ],
      "categories": [
        {
          "id": 11
        },
        {
          "id": 13
        }
      ],
      "images": [
        {
          "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/cd_4_angle.jpg"
        }
      ]
    },
    {
      "name": "New Premium Quality",
      "type": "simple",
      "regular_price": "21.99",
      "description": "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.",
      "short_description": "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.",
      "categories": [
        {
          "id": 9
        },
        {
          "id": 14
        }
      ],
      "images": [
        {
          "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_front.jpg"
        },
        {
          "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_back.jpg"
        }
      ]
    }
  ],
  "update": [
    {
      "id": 799,
      "default_attributes": [
        {
          "id": 6,
          "name": "Color",
          "option": "Green"
        },
        {
          "id": 0,
          "name": "Size",
          "option": "M"
        }
      ]
    }
  ],
  "delete": [
    794
  ]
}'
```

```javascript
const data = {
  create: [
    {
      name: "Woo Single #1",
      type: "simple",
      regular_price: "21.99",
      virtual: true,
      downloadable: true,
      downloads: [
        {
          name: "Woo Single",
          file: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/cd_4_angle.jpg"
        }
      ],
      categories: [
        {
          id: 11
        },
        {
          id: 13
        }
      ],
      images: [
        {
          src: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/cd_4_angle.jpg"
        }
      ]
    },
    {
      name: "New Premium Quality",
      type: "simple",
      regular_price: "21.99",
      description: "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.",
      short_description: "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.",
      categories: [
        {
          id: 9
        },
        {
          id: 14
        }
      ],
      images: [
        {
          src: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_front.jpg"
        },
        {
          src: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_back.jpg"
        }
      ]
    }
  ],
  update: [
    {
      id: 799,
      default_attributes: [
        {
          id: 6,
          name: "Color",
          option: "Green"
        },
        {
          id: 0,
          name: "Size",
          option: "M"
        }
      ]
    }
  ],
  delete: [
    794
  ]
};

WooCommerce.post("products/batch", data)
  .then((response) => {
    console.log(response.data);
  })
  .catch((error) => {
    console.log(error.response.data);
  });
```

```php
<?php
$data = [
    'create' => [
        [
            'name' => 'Woo Single #1',
            'type' => 'simple',
            'regular_price' => '21.99',
            'virtual' => true,
            'downloadable' => true,
            'downloads' => [
                [
                    'name' => 'Woo Single',
                    'file' => 'http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/cd_4_angle.jpg'
                ]
            ],
            'categories' => [
                [
                    'id' => 11
                ],
                [
                    'id' => 13
                ]
            ],
            'images' => [
                [
                    'src' => 'http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/cd_4_angle.jpg'
                ]
            ]
        ],
        [
            'name' => 'New Premium Quality',
            'type' => 'simple',
            'regular_price' => '21.99',
            'description' => 'Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.',
            'short_description' => 'Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.',
            'categories' => [
                [
                    'id' => 9
                ],
                [
                    'id' => 14
                ]
            ],
            'images' => [
                [
                    'src' => 'http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_front.jpg'
                ],
                [
                    'src' => 'http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_back.jpg'
                ]
            ]
        ]
    ],
    'update' => [
        [
            'id' => 799,
            'default_attributes' => [
                [
                    'id' => 6,
                    'name' => 'Color',
                    'option' => 'Green'
                ],
                [
                    'id' => 0,
                    'name' => 'Size',
                    'option' => 'M'
                ]
            ]
        ]
    ],
    'delete' => [
        794
    ]
];

print_r($woocommerce->post('products/batch', $data));
?>
```

```python
data = {
    "create": [
        {
            "name": "Woo Single #1",
            "type": "simple",
            "regular_price": "21.99",
            "virtual": True,
            "downloadable": True,
            "downloads": [
                {
                    "name": "Woo Single",
                    "file": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/cd_4_angle.jpg"
                }
            ],
            "categories": [
                {
                    "id": 11
                },
                {
                    "id": 13
                }
            ],
            "images": [
                {
                    "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/cd_4_angle.jpg"
                }
            ]
        },
        {
            "name": "New Premium Quality",
            "type": "simple",
            "regular_price": "21.99",
            "description": "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.",
            "short_description": "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.",
            "categories": [
                {
                    "id": 9
                },
                {
                    "id": 14
                }
            ],
            "images": [
                {
                    "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_front.jpg"
                },
                {
                    "src": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_back.jpg"
                }
            ]
        }
    ],
    "update": [
        {
            "id": 799,
            "default_attributes": [
                {
                    "id": 6,
                    "name": "Color,
                    "option": "Green"
                },
                {
                    "id": 0,
                    "name": "Size",
                    "option": "M"
                }
            ]
        }
    ],
    "delete": [
        794
    ]
}

print(wcapi.post("products/batch", data).json())
```

```ruby
data = {
  create: [
    {
      name: "Woo Single #1",
      type: "simple",
      regular_price: "21.99",
      virtual: true,
      downloadable: true,
      downloads: [
        {
          name: "Woo Single",
          file: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/cd_4_angle.jpg"
        }
      ],
      categories: [
        {
          id: 11
        },
        {
          id: 13
        }
      ],
      images: [
        {
          src: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/cd_4_angle.jpg"
        }
      ]
    },
    {
      name: "New Premium Quality",
      type: "simple",
      regular_price: "21.99",
      description: "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.",
      short_description: "Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.",
      categories: [
        {
          id: 9
        },
        {
          id: 14
        }
      ],
      images: [
        {
          src: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_front.jpg"
        },
        {
          src: "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/T_2_back.jpg"
        }
      ]
    }
  ],
  update: [
    {
      id: 799,
      default_attributes: [
        {
          id: 6,
          name: "Color,
          option: "Green"
        },
        {
          id: 0,
          name: "Size",
          option: "M"
        }
      ]
    }
  ],
  delete: [
    794
  ]
}

woocommerce.post("products/batch", data).parsed_response
```

> JSON response example:

```json
{
  "create": [
    {
      "id": 801,
      "name": "Woo Single #1",
      "slug": "woo-single-1-4",
      "permalink": "https://example.com/product/woo-single-1-4/",
      "date_created": "2017-03-23T17:35:43",
      "date_created_gmt": "2017-03-23T20:35:43",
      "date_modified": "2017-03-23T17:35:43",
      "date_modified_gmt": "2017-03-23T20:35:43",
      "type": "simple",
      "status": "publish",
      "featured": false,
      "catalog_visibility": "visible",
      "description": "",
      "short_description": "",
      "sku": "",
      "price": "21.99",
      "regular_price": "21.99",
      "sale_price": "",
      "date_on_sale_from": null,
      "date_on_sale_from_gmt": null,
      "date_on_sale_to": null,
      "date_on_sale_to_gmt": null,
      "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>21.99</span>",
      "on_sale": false,
      "purchasable": true,
      "total_sales": 0,
      "virtual": true,
      "downloadable": true,
      "downloads": [
        {
          "id": 0,
          "name": "Woo Single",
          "file": "http://demo.woothemes.com/woocommerce/wp-content/uploads/sites/56/2013/06/cd_4_angle.jpg"
        }
      ],
      "download_limit": -1,
      "download_expiry": -1,
      "external_url": "",
      "button_text": "",
      "tax_status": "taxable",
      "tax_class": "",
      "manage_stock": false,
      "stock_quantity": null,
      "stock_status": "instock",
      "backorders": "no",
      "backorders_allowed": false,
      "backordered": false,
      "sold_individually": false,
      "weight": "",
      "dimensions": {
        "length": "",
        "width": "",
        "height": ""
      },
      "shipping_required": false,
      "shipping_taxable": true,
      "shipping_class": "",
      "shipping_class_id": 0,
      "reviews_allowed": true,
      "average_rating": "0.00",
      "rating_count": 0,
      "related_ids": [
        588,
        87,
        573,
        96,
        329
      ],
      "upsell_ids": [],
      "cross_sell_ids": [],
      "parent_id": 0,
      "purchase_note": "",
      "categories": [
        {
          "id": 11,
          "name": "Music",
          "slug": "music"
        },
        {
          "id": 13,
          "name": "Singles",
          "slug": "singles"
        }
      ],
      "tags": [],
      "images": [
        {
          "id": 800,
          "date_created": "2017-03-23T14:35:43",
          "date_created_gmt": "2017-03-23T20:35:43",
          "date_modified": "2017-03-23T14:35:43",
          "date_modified_gmt": "2017-03-23T20:35:43",
          "src": "https://example.com/wp-content/uploads/2017/03/cd_4_angle.jpg",
          "name": "",
          "alt": ""
        }
      ],
      "attributes": [],
      "default_attributes": [],
      "variations": [],
      "grouped_products": [],
      "menu_order": 0,
      "meta_data": [],
      "_links": {
        "self": [
          {
            "href": "https://example.com/wp-json/wc/v3/products/801"
          }
        ],
        "collection": [
          {
            "href": "https://example.com/wp-json/wc/v3/products"
          }
        ]
      }
    },
    {
      "id": 804,
      "name": "New Premium Quality",
      "slug": "new-premium-quality",
      "permalink": "https://example.com/product/new-premium-quality/",
      "date_created": "2017-03-23T17:35:48",
      "date_created_gmt": "2017-03-23T20:35:48",
      "date_modified": "2017-03-23T17:35:48",
      "date_modified_gmt": "2017-03-23T20:35:48",
      "type": "simple",
      "status": "publish",
      "featured": false,
      "catalog_visibility": "visible",
      "description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>\n",
      "short_description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>\n",
      "sku": "",
      "price": "21.99",
      "regular_price": "21.99",
      "sale_price": "",
      "date_on_sale_from": null,
      "date_on_sale_from_gmt": null,
      "date_on_sale_to": null,
      "date_on_sale_to_gmt": null,
      "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>21.99</span>",
      "on_sale": false,
      "purchasable": true,
      "total_sales": 0,
      "virtual": false,
      "downloadable": false,
      "downloads": [],
      "download_limit": -1,
      "download_expiry": -1,
      "external_url": "",
      "button_text": "",
      "tax_status": "taxable",
      "tax_class": "",
      "manage_stock": false,
      "stock_quantity": null,
      "stock_status": "instock",
      "backorders": "no",
      "backorders_allowed": false,
      "backordered": false,
      "sold_individually": false,
      "weight": "",
      "dimensions": {
        "length": "",
        "width": "",
        "height": ""
      },
      "shipping_required": true,
      "shipping_taxable": true,
      "shipping_class": "",
      "shipping_class_id": 0,
      "reviews_allowed": true,
      "average_rating": "0.00",
      "rating_count": 0,
      "related_ids": [
        458,
        56,
        99,
        34,
        378
      ],
      "upsell_ids": [],
      "cross_sell_ids": [],
      "parent_id": 0,
      "purchase_note": "",
      "categories": [
        {
          "id": 9,
          "name": "Clothing",
          "slug": "clothing"
        },
        {
          "id": 14,
          "name": "T-shirts",
          "slug": "t-shirts"
        }
      ],
      "tags": [],
      "images": [
        {
          "id": 802,
          "date_created": "2017-03-23T14:35:47",
          "date_created_gmt": "2017-03-23T20:35:47",
          "date_modified": "2017-03-23T14:35:47",
          "date_modified_gmt": "2017-03-23T20:35:47",
          "src": "https://example.com/wp-content/uploads/2017/03/T_2_front-5.jpg",
          "name": "",
          "alt": ""
        },
        {
          "id": 803,
          "date_created": "2017-03-23T14:35:48",
          "date_created_gmt": "2017-03-23T20:35:48",
          "date_modified": "2017-03-23T14:35:48",
          "date_modified_gmt": "2017-03-23T20:35:48",
          "src": "https://example.com/wp-content/uploads/2017/03/T_2_back-3.jpg",
          "name": "",
          "alt": ""
        }
      ],
      "attributes": [],
      "default_attributes": [],
      "variations": [],
      "grouped_products": [],
      "menu_order": 0,
      "meta_data": [],
      "_links": {
        "self": [
          {
            "href": "https://example.com/wp-json/wc/v3/products/804"
          }
        ],
        "collection": [
          {
            "href": "https://example.com/wp-json/wc/v3/products"
          }
        ]
      }
    }
  ],
  "update": [
    {
      "id": 799,
      "name": "Ship Your Idea",
      "slug": "ship-your-idea-22",
      "permalink": "https://example.com/product/ship-your-idea-22/",
      "date_created": "2017-03-23T17:03:12",
      "date_created_gmt": "2017-03-23T20:03:12",
      "date_modified": "2017-03-23T17:03:12",
      "date_modified_gmt": "2017-03-23T20:03:12",
      "type": "variable",
      "status": "publish",
      "featured": false,
      "catalog_visibility": "visible",
      "description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>\n",
      "short_description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>\n",
      "sku": "",
      "price": "",
      "regular_price": "",
      "sale_price": "",
      "date_on_sale_from": null,
      "date_on_sale_from_gmt": null,
      "date_on_sale_to": null,
      "date_on_sale_to_gmt": null,
      "price_html": "",
      "on_sale": false,
      "purchasable": false,
      "total_sales": 0,
      "virtual": false,
      "downloadable": false,
      "downloads": [],
      "download_limit": -1,
      "download_expiry": -1,
      "external_url": "",
      "button_text": "",
      "tax_status": "taxable",
      "tax_class": "",
      "manage_stock": false,
      "stock_quantity": null,
      "stock_status": "instock",
      "backorders": "no",
      "backorders_allowed": false,
      "backordered": false,
      "sold_individually": false,
      "weight": "",
      "dimensions": {
        "length": "",
        "width": "",
        "height": ""
      },
      "shipping_required": true,
      "shipping_taxable": true,
      "shipping_class": "",
      "shipping_class_id": 0,
      "reviews_allowed": true,
      "average_rating": "0.00",
      "rating_count": 0,
      "related_ids": [
        414,
        40,
        34,
        463,
        15
      ],
      "upsell_ids": [],
      "cross_sell_ids": [],
      "parent_id": 0,
      "purchase_note": "",
      "categories": [
        {
          "id": 9,
          "name": "Clothing",
          "slug": "clothing"
        },
        {
          "id": 14,
          "name": "T-shirts",
          "slug": "t-shirts"
        }
      ],
      "tags": [],
      "images": [
        {
          "id": 795,
          "date_created": "2017-03-23T14:03:08",
          "date_created_gmt": "2017-03-23T20:03:08",
          "date_modified": "2017-03-23T14:03:08",
          "date_modified_gmt": "2017-03-23T20:03:08",
          "src": "https://example.com/wp-content/uploads/2017/03/T_4_front-11.jpg",
          "name": "",
          "alt": ""
        },
        {
          "id": 796,
          "date_created": "2017-03-23T14:03:09",
          "date_created_gmt": "2017-03-23T20:03:09",
          "date_modified": "2017-03-23T14:03:09",
          "date_modified_gmt": "2017-03-23T20:03:09",
          "src": "https://example.com/wp-content/uploads/2017/03/T_4_back-10.jpg",
          "name": "",
          "alt": ""
        },
        {
          "id": 797,
          "date_created": "2017-03-23T14:03:10",
          "date_created_gmt": "2017-03-23T20:03:10",
          "date_modified": "2017-03-23T14:03:10",
          "date_modified_gmt": "2017-03-23T20:03:10",
          "src": "https://example.com/wp-content/uploads/2017/03/T_3_front-10.jpg",
          "name": "",
          "alt": ""
        },
        {
          "id": 798,
          "date_created": "2017-03-23T14:03:11",
          "date_created_gmt": "2017-03-23T20:03:11",
          "date_modified": "2017-03-23T14:03:11",
          "date_modified_gmt": "2017-03-23T20:03:11",
          "src": "https://example.com/wp-content/uploads/2017/03/T_3_back-10.jpg",
          "name": "",
          "alt": ""
        }
      ],
      "attributes": [
        {
          "id": 6,
          "name": "Color",
          "position": 0,
          "visible": false,
          "variation": true,
          "options": [
            "Black",
            "Green"
          ]
        },
        {
          "id": 0,
          "name": "Size",
          "position": 0,
          "visible": true,
          "variation": true,
          "options": [
            "S",
            "M"
          ]
        }
      ],
      "default_attributes": [
        {
          "id": 6,
          "name": "Color",
          "option": "green"
        },
        {
          "id": 0,
          "name": "Size",
          "option": "M"
        }
      ],
      "variations": [],
      "grouped_products": [],
      "menu_order": 0,
      "meta_data": [],
      "_links": {
        "self": [
          {
            "href": "https://example.com/wp-json/wc/v3/products/799"
          }
        ],
        "collection": [
          {
            "href": "https://example.com/wp-json/wc/v3/products"
          }
        ]
      }
    }
  ],
  "delete": [
    {
      "id": 794,
      "name": "Premium Quality",
      "slug": "premium-quality-19",
      "permalink": "https://example.com/product/premium-quality-19/",
      "date_created": "2017-03-23T17:01:14",
      "date_created_gmt": "2017-03-23T20:01:14",
      "date_modified": "2017-03-23T17:01:14",
      "date_modified_gmt": "2017-03-23T20:01:14",
      "type": "simple",
      "status": "publish",
      "featured": false,
      "catalog_visibility": "visible",
      "description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>\n",
      "short_description": "<p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.</p>\n",
      "sku": "",
      "price": "24.54",
      "regular_price": "24.54",
      "sale_price": "",
      "date_on_sale_from": null,
      "date_on_sale_from_gmt": null,
      "date_on_sale_to": null,
      "date_on_sale_to_gmt": null,
      "price_html": "<span class=\"woocommerce-Price-amount amount\"><span class=\"woocommerce-Price-currencySymbol\">&#36;</span>24.54</span>",
      "on_sale": false,
      "purchasable": true,
      "total_sales": 0,
      "virtual": false,
      "downloadable": false,
      "downloads": [],
      "download_limit": -1,
      "download_expiry": -1,
      "external_url": "",
      "button_text": "",
      "tax_status": "taxable",
      "tax_class": "",
      "manage_stock": false,
      "stock_quantity": null,
      "stock_status": "instock",
      "backorders": "no",
      "backorders_allowed": false,
      "backordered": false,
      "sold_individually": false,
      "weight": "",
      "dimensions": {
        "length": "",
        "width": "",
        "height": ""
      },
      "shipping_required": true,
      "shipping_taxable": true,
      "shipping_class": "",
      "shipping_class_id": 0,
      "reviews_allowed": true,
      "average_rating": "0.00",
      "rating_count": 0,
      "related_ids": [
        369,
        56,
        378,
        31,
        22
      ],
      "upsell_ids": [],
      "cross_sell_ids": [],
      "parent_id": 0,
      "purchase_note": "",
      "categories": [
        {
          "id": 9,
          "name": "Clothing",
          "slug": "clothing"
        },
        {
          "id": 14,
          "name": "T-shirts",
          "slug": "t-shirts"
        }
      ],
      "tags": [],
      "images": [
        {
          "id": 792,
          "date_created": "2017-03-23T14:01:13",
          "date_created_gmt": "2017-03-23T20:01:13",
          "date_modified": "2017-03-23T14:01:13",
          "date_modified_gmt": "2017-03-23T20:01:13",
          "src": "https://example.com/wp-content/uploads/2017/03/T_2_front-4.jpg",
          "name": "",
          "alt": ""
        },
        {
          "id": 793,
          "date_created": "2017-03-23T14:01:14",
          "date_created_gmt": "2017-03-23T20:01:14",
          "date_modified": "2017-03-23T14:01:14",
          "date_modified_gmt": "2017-03-23T20:01:14",
          "src": "https://example.com/wp-content/uploads/2017/03/T_2_back-2.jpg",
          "name": "",
          "alt": ""
        }
      ],
      "attributes": [],
      "default_attributes": [],
      "variations": [],
      "grouped_products": [],
      "menu_order": 0,
      "meta_data": [],
      "_links": {
        "self": [
          {
            "href": "https://example.com/wp-json/wc/v3/products/794"
          }
        ],
        "collection": [
          {
            "href": "https://example.com/wp-json/wc/v3/products"
          }
        ]
      }
    }
  ]
}
```
