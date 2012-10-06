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

<table border="1" cellspacing="5" cellpadding="5">
	<tr>
		<th>Method</th><th>Sample output</th><th>Notes</th>
	</tr>
	<tr>
		<td><code>GetRandomDouble()</code></td>
		<td>0.5245344487598792</td>
		<td></td>
	</tr>
	<tr>
		<td><code>GetRandomGuid([format])</code></td>
		<td>dadb6c43-137b-440d-9bee-9542554ac7fd</td>
		<td></td>
	</tr>
	<tr>
		<td><code>GetRandomNumber()</code></td>
		<td>474184758</td>
		<td></td>
	</tr>
	<tr>
		<td><code>GetRandomNumber(maximum)</code></td>
		<td>7</td>
		<td></td>
	</tr>
	<tr>
		<td><code>GetRandomNumber(minimum, maximum)</code></td>
		<td>90</td>
		<td>Between <var>minimum</var> and <var>maximum</var>, including both</td>
	</tr>
	<tr>
		<td><code>GetRandomNumbers(count)</code></td>
		<td>3,1,4,2</td>
		<td>The numbers from 1 to <var>count</var>, ordered randomly in a CSV list</td>
	</tr>
	<tr>
		<td><code>GetRandomNumbersAsXml(count)</code></td>
		<td>
<pre><code>&lt;values&gt;
	&lt;value&gt;3&lt;/value&gt;
	&lt;value&gt;4&lt;/value&gt;
	&lt;value&gt;5&lt;/value&gt;
	&lt;value&gt;1&lt;/value&gt;
	&lt;value&gt;2&lt;/value&gt;
&lt;/values&gt;
</code></pre>
</td>
		<td>The numbers from 1 to <var>count</var> as a randomly ordered nodeset</td>
	</tr>
	<tr>
		<td><code>GetRandomString(count)</code></td>
		<td>yzy</td>
		<td>A random string of <var>count</var> characters</td>
	</tr>
</table>