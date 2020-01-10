# Helpers

### optional helper

[Laravel docs](https://laravel.com/docs/6.x/helpers#method-optional)

Laravel's optional helper method is very useful to handle null value.

```
return optional($user->address)->street;
```

```
return optional(User::find($id), function ($user) {
    return new DummyUser;
});
```

### data_get helper

[Laravel docs](https://laravel.com/docs/6.x/helpers#method-data-get)

It's very useful on accessing the array.

Before, example
```
$data = ['products' => ['desk' => ['price' => 100]]];
$price = isset($data['products']['desk']['price']) ? $data['products']['desk']['price'] : null;
```

After, example

```
$data = ['products' => ['desk' => ['price' => 100]]];

$price = data_get($data, 'products.desk.price');
```