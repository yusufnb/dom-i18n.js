About
===========

dom-i18n.js is an element attribute based i18n plugin. It is intended to be used as an extension of client side templating libraries such as Mustache.js. It greatly simplifies i18n for web apps and allows changing languages without page refreshes or without writing little to no code for adding i18n support.

Dependency
==========
 - jQuery

Note
==========
This plugin/library does not do any magic. It should be integrated with your web app framework and passed appropriate data. Here are few places it will need integration:
- app boot process, to initialize i18n and load a language
- On language change. i18n does not read browser language changes or any other events. The app framework should handle that and invoke corresponding APIs.
- i18n.format.js is an add-on plugin and is completely optional

Setup:
======
```
i18n.config({
  url: 'http://example.com/locales/', // Pull content from http://example.com/locales/en.json
  
});

i18n.load('en', {...});
i18n.load('en'); // Load from cache or ajax on URL

i18n.parse(selector);

i18n.parse(element);
```

Usage:
======

```
<span i18n="HelloWorld" />
```

```
<span i18n="HelloWorld > placeholder" />
```

```
HelloWorld="Hello World {#} {#}"
<span i18n="HelloWorld | aa | bb" />
```
```
HelloWorld="Hello World {#:date} {#:currency}
```
