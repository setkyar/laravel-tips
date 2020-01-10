# Eloquent


### Chained where


Example,

```
$articles = Article::where('name', 'Universe')
				->where('email', '=', 'me@setkyar.com')
				->get()
```

That one can improve to...
```
Article::where([
	'name' => 'Universe, 
	['email', '=', 'me@setkyar.com'
])->get();
```