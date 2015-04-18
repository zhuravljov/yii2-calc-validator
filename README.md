Yii2 Calc Validator
===================

Math expression validator without using `eval()` for Yii2.

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
$ composer require zhuravljov/calc
```

or add

```
"zhuravljov/calc": "*"
```

to the `require` section of your `composer.json` file.

Usage
-----

```php
public function rules()
{
    return [
        // ...
        
        // Rule for checking an expression
        ['amount1', 'zhuravljov\yii\validators\CalcValidator'],

        // Rule for checking an expressions with saving result of calculation
        ['amount2', 'zhuravljov\yii\validators\CalcValidator', 'resultAttribute' => 'amount2'],
        
        // ...
    ];
}
```