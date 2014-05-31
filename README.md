angular-intro-plus.js
================

An angularjs directive that wraps [intro.js](http://usablica.github.io/intro.js/) functionality.

![angularintroplus](http://farm8.staticflickr.com/7382/9741892196_ccc16b8a16_o.png)

See [the demo page](http://angular-intro.iamdenny.com/) for an overview.


## Details

The two main directives are `ng-intro-plus-options` and `ng-intro-plus-show`.

`ng-intro-plus-options` needs to point at a `$scope` object which contains the intro.js options. The options are exactly the same as [the original](https://github.com/usablica/intro.js#options).  This also allows you to modify the options as part of your controller behavior if necessary.

`ng-intro-plus-show` is a method name that you want to use later.  In other words, put any name in there that doesn't exist on the `$scope` already.  The directive will create a method with that name so that you can call it yourself later.

For example, if you set `ng-intro-plus-show="CallMe"`, then you can later call `ng-click="CallMe();"` as long as you are still in the same controller scope.

To start the intro from code, either call `$scope.CallMe();` or set `ng-intro-plus-autostart="true"`.  If the `$scope.CallMe();` doesn't work, it might be because your DOM isn't ready. Put it in a `$timeout`.

There are also directives that link to the intro.js callbacks, namely `ng-intro-plus-oncomplete`, `ng-intro-plus-onexit`, `ng-intro-plus-onchange` `ng-intro-plus-onbeforechange` and `ng-intro-plus-onafterchange`.


## License

As with intro.js and angular-intro.js, this is under the [MIT license](https://github.com/iamdenny/angular-intro-plus.js/blob/master/LICENSE).






