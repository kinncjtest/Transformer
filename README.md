Transformer
===========

A PHP DataType transformer

```php
<?php
class Foo
{
 public $bar="Baz";
}
$foo      = new Foo;
$t        = new Transformer($foo);
$stdClass = $t->to("stdClass");

$serialized = serialize($foo);
$t          = new Transformer($serialized);
$stdClass   = $t->to("stdClass");

$json     = serialize($foo);
$t        = new Transformer($json);
$stdClass = $t->to("stdClass");

class Xuplau {}

$json     = serialize($foo);
$t        = new Transformer($json);
xuplau    = $t->to("Xuplau");
```
