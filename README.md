# LaraOutPress (Laravel Output Press)
This is simply compress your final out of Larvel Application and serve to the browser.

### How to install

~~~bash
	composer require vrkansagara/lara-out-press
~~~

### How to activate this compression middleware in your application

Update your `app/Http/Kernel.php` file with below line

~~~php
protected $middleware = [
	...
        \Vrkansagara\Http\Middleware\AfterMiddleware::class,
    	...
    ];
~~~

Add your target environment into `.env`
~~~bash
    VRKANSAGARA_COMPRESS_ENVIRONMENT='prod,testing,dev,local'
~~~


If you want to see how much you compress on each page, set bellow line in `.env`
~~~bash
    VRKANSAGARA_COMPRESS_DEBUG=0
~~~


### Display usage on each page.

Set `$debug = 1;` in `AfterMiddleware.php`


### TO Do List

- [x] Compress browser output.
- [] Combile all CSS
- [] Combile all JavaScript files.
- [] Compress using varis algorithms.
- [] Versioning the compress file.
- [] Excempt route(s),middleware,group,prefix

### Task

- [x] Add analytics before compress and after compress.

### Code Assumption
This code is developed with the mind set of each request is filtered by this middleware. So most of the code will not be flexi.

Improvement and suggestion are alwayse welcome. 
