# Product custom fields #

The product custom fields API allows you to view the custom fields that have been recorded.

## Product custom fields properties ##

| Attribute | Type   | Description                                                                                                 |
| --------- | ------ | ----------------------------------------------------------------------------------------------------------- |
| `key`     | string | The custom field key.                                                                                       |
| `value`   | string | The value set for the key.                                                                                  |

## Retrieve product custom fields ##

This API lets you retrieve filtered custom fields.

<div class="api-endpoint">
	<div class="endpoint-data">
		<i class="label label-get">GET</i>
		<h6>/wp-json//wc/v3/products/custom-fields/names</h6>
	</div>
</div>

```shell
curl https://example.com/wp-json/wc/v3/products/custom-fields/names \
	-u consumer_key:consumer_secret
```

```javascript
WooCommerce.get("products/custom-fields/names")
  .then((response) => {
    console.log(response.data);
  })
  .catch((error) => {
    console.log(error.response.data);
  });
```

```php
<?php print_r($woocommerce->get('products/custom-fields/names')); ?>
```

```python
print(wcapi.get("products/custom-fields/names").json())
```

```ruby
woocommerce.get("products/custom-fields/names").parsed_response
```

> JSON response example:

```json
{
	[
		"Custom field 1",
		"Custom field 2",
		"Custom field 3",
		"Custom field 4"
	]
}
```
