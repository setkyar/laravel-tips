# Request Handling

When handing the request, Most of the time we use `request->only()` with the very long array. Instead, why not we create a separate method? Much cleaner and more reusable?

Before...

```
$userData = request([
	'name',
	'email',
	'address',
	'phone',
]);
```


After...

```
$userData = request($this->getUserFields());

protected function getUserFields()
{
	return [
		'name',
		'email',
		'address',
		'phone',
	];
}
```