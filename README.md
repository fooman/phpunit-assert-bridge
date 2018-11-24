# How to Use

The aim is to be able to write phpunit assertions for phpunit 6 and then be able to run these for Magento 2.3 and earlier (more accurately their associated phpunit versions).

Install with

```
composer require fooman/phpunit-assert-bridge --dev
```

and then instead of `\PHPUnit\Framework\Assert` or `\PHPUnit_Framework_Assert` use `Fooman\PhpunitAssertBridge\CompatAssert` in both cases.


```
<?php

use Fooman\PhpunitAssertBridge\CompatAssert;

class MyTestCaseAssertion extends extends \Magento\Mtf\Constraint\AbstractConstraint
{

    public function processAssert(
    	...
	) {
    	CompatAssert::assertEquals('expected', $actual);			
	}

}
```
