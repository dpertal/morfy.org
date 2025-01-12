---
title: Arr
description: Documentation for Morfy Developers and Morfy Users.
keywords: documentation, development, lessons, faq, cms, questions
template: documentation
---

The array class contains methods that can be useful when working with arrays.

Subval sort
```
$new_array = Arr::subvalSort($old_array, 'sort');
```

Return value from array using "dot notation".
If the key does not exist in the array, the default value will be returned instead.
```
$login = Arr::get($_POST, 'login');

$array = array('foo' => 'bar');
$foo = Arr::get($array, 'foo');

$array = array('test' => array('foo' => 'bar'));
$foo = Arr::get($array, 'test.foo');
```

Delete an array value using "dot notation".
```
Arr::delete($array, 'foo.bar');
```

Checks if the given dot-notated key exists in the array.
```
if (Arr::keyExists($array, 'foo.bar')) {
    // Do something...
}
```

Returns a random value from an array.
```
$random = Arr::random(array('php', 'js', 'css', 'html'));
```

Returns TRUE if the array is associative and FALSE if not.
```
if (Arr::isAssoc($array)) {
    // Do something...
}
```
