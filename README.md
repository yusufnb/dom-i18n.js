dom-i18n.js
===========

DOM element attribute based i18n plugin

Dependency:
==========
 - jQuery

Setup:
======
```
i18n.config({
  url: 'http://example.com/locales/', // Pull content from http://example.com/locales/en.json
  
});

i18n.load('en', {...});
i18n.load('en'); // Load from cache or ajax on URL
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
