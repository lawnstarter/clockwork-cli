Clockwork-cli
=============

Command-line interface for Clockwork. Useful for visualizing clockwork logs for apps with no frontend (like APIs).

This is a fork of [Petr Trofimov's repository](https://github.com/ptrofimov/clockwork-cli), modified to work with Laravel 5.

**[Clockwork](http://github.com/itsgoingd/clockwork)** - is a tool for debugging and profiling PHP applications.

**[Clockwork-chrome](http://github.com/itsgoingd/clockwork-chrome)** - is a Chrome extension for Clockwork.

**[Clockwork-firebug](https://github.com/sidorovich/clockwork-firebug)** - it's Clockwork extension for Firebug.


## Installation

* Add the repo to your composer.json:
```
{
    "type": "vcs",
    "url": "https://github.com/lawnstarter/clockwork-cli"
}
```

Install clockwork-cli via composer for your project:
```
composer require lawnstarter/clockwork-cli:*
```

* Register the artisan command in app\Console\Kernel.php:
```
\Clockwork\Cli\Laravel\Command::class,
```

## Usage

* Run script to monitor clockwork logs for current project:
```
php artisan clockwork:log
```

* You will see updating list of HTTP requests. The first character is a hotkey.
* Press the hotkey to view details of HTTP request.
* Press Backspace to show requests for last 10 minutes
* Press Escape to exit

## Screenshots

![Clockwork Cli Trace](https://raw.githubusercontent.com/ptrofimov/clockwork-cli/master/screenshots/clockwork-cli-trace.png)

![Clockwork Cli Details](https://raw.githubusercontent.com/ptrofimov/clockwork-cli/master/screenshots/clockwork-cli-details.png)

## License

Copyright (c) 2014 Petr Trofimov

MIT License

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
