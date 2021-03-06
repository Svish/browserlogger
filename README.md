Overview
===

![Latest version](https://poser.pugx.org/geekality/consolelog/version?format=flat-square)
![Downloads](https://poser.pugx.org/geekality/consolelog/downloads?format=flat-square)
![License](https://poser.pugx.org/geekality/consolelog/license?format=flat-square)


Allows easy server-side logging to browsers supporting the [Chrome Logger](http://www.chromelogger.com) protocol. Either native or via plugins.


Usage
===

```php
use Geekality\ConsoleLog;

ConsoleLog::info('Hello console!');
ConsoleLog::log($_SERVER);
ConsoleLog::warn('something is off with', $object);
ConsoleLog::error('fail');

ConsoleLog::table([
	['R1 C1', 'R1 C2'],
	['R2 C1', 'R2 C2'],
	]);

ConsoleLog::group('Group header');
ConsoleLog::log('Bar');
ConsoleLog::groupEnd();

```

See more examples in [sample/index.php](sample/index.php).

-------


Source
---

Based on [ccampbell/chromephp](http://github.com/ccampbell/chromephp), but more or less a complete rewrite because I found that one hard to extend and adjust in my own project. 😟

Ended up using newer PHP features and simplifying it a bit too, because that's how I roll.

Also called it `ConsoleLog` because I find it weird to use `Chrome` and `Php` in my code, when already writing PHP and I'm viewing the messages in the native Developer Console in FireFox... 🤔 🙂


