# PHP in General

### PHP Dynamic method calling

Can use on various stuff but very handy on handling condition

Example...

```
if($role === 'admin') {
    //Do admin related stuff
} else if ($role === 'user') {
    //do user related stuff
} else {
    //do something else
}
```

With dynamic method calling, we can do something like the following

```
if(method_exists($this, $method = 'handle{ucfirst($role)}Stuff')) {
    $this->{$method}();
}

//do something else

protected function handleAdminStuff()
{
	//Do admin related stuff
}

protected function handleUserStuff()
{
	//do user related stuff
}
```