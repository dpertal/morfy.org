---
title: Token
description: Documentation for Morfy Developers and Morfy Users.
keywords: documentation, development, lessons, faq, cms, questions
template: documentation
---
Generate and store a unique token which can be used to help prevent  
[CSRF](http://wikipedia.org/wiki/Cross_Site_Request_Forgery) attacks.  

```
$token = Token::generate();
```

You can insert this token into your forms as a hidden field:  
```
<input type="hidden" name="csrf" value="<?php echo Token::generate(); ?>">
```

Check that the given token matches the currently stored security token.  
```
if (Token::check($token)) {
    // Pass
}
```
