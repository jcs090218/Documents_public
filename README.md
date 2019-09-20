I have been using Emacs since 2015 and this configuration is the result after these few years of living inside Emacs. I don't think this configuration will ever satisfy anyone, neither do I. But I feel really great with what I am doing here and wanting to share how great this configuration benefits me in my daily life of programming.

You can find it on  [https://github.com/jcs090218/jcs-emacs-init](https://github.com/jcs090218/jcs-emacs-init) 

Current version is `5.8.4`.

### Features

* Out of box.
* Short startup time. (Lazy Loading)
* Support multiple programming languages. (Mostly all programming languages I used)
  * ActionScript 2.0 or 3.0 / Assembly Language
  * BASIC / Batchfile
  * C / C++ / C# / Clojure / CMake / COBOL / CSS
  * Dart
  * Elixir / Emacs Lisp / Erlang
  * ...
* Auto completion (company)
* Better `*dashboard*` support.
* Better `org` support.
* Better `buffer-menu` support.
* Flycheck integration.
* Projectile integration.
* Fuzzy `helm`/`company`
* ...

There are very many details in this config; I couldn't list them all out. For example, `kill-buffer` is executed if this buffer is 
shown in one window; otherwise, `bury-buffer` is executed. (This may be weird to someone, but this make a lot more sense to me :P)

### Links

* All integrations, see [here](https://github.com/jcs090218/jcs-emacs-init#powered-by). (Include `magit`, `sr-speedbar`, `quelpa`, `regexp` etc.)
* If you willing to try out this config please checkout the keybindings document [here](https://github.com/jcs090218/jcs-emacs-init/blob/master/doc/keybindings.md).
* All supported languages should be listed [here](https://github.com/jcs090218/jcs-emacs-init/blob/master/doc/programming_modes.md).
