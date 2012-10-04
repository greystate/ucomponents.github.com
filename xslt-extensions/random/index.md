---
layout: extension
title: Random
category: XSLT Extensions
---

The Random library XSLT extension can be used to generate various types of random numbers.

## Enabling the XSLT extension for use in your XSLT templates.

Add the following XML snippet to your `~/config/xsltExtensions.config` file:

	<XsltExtensions>
		...
		<ext assembly="uComponents.Core" type="uComponents.Core.XsltExtensions.Random" alias="ucomponents.random" />
		...
	</XsltExtensions>

The following methods are available:

* `GetRandomDouble()`
* `GetRandomGuid([format])`
* `GetRandomNumber()`
* `GetRandomNumber(maximum)`
* `GetRandomNumber(minimum, maximum)`
* `GetRandomNumbers(count)`
* `GetRandomNumbersAsXml(count)`
* `GetRandomString(count)`
