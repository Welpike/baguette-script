# Plugin development

There is the basic code base for a plugin.

```js
///=========================================================================
/// Plugin information (author, date, description, version, etc...)
///=========================================================================

'use strict';

(function (self, factory) {
    const plugin = factory(self);

    if (typeof exports === 'object' && typeof exports['nodeName'] !== 'string') {
		module.exports = plugin
	} else {
		if ('baguetteScript' in self) self.baguetteScript.use(plugin)
    }
})(typeof self !== 'undefined' ? self : this, self => {
	return (baguetteScript) => {
       // here put your commands/features/etc...
    }
})
```
