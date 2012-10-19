---
layout: extension
title: Random
category: XSLT Extensions

extassembly: uComponents.Core
exttype: uComponents.Core.XsltExtensions.Random
extalias: ucomponents.random
extprefix: ucom.random
---

The Random library XSLT extension can be used to generate various types of random numbers.

{% include enable-xslt-extension.md %}

### Available methods

The following methods are available:

* `GetRandomDouble()`
* `GetRandomGuid(format)`
* `GetRandomNumber(maximum)`
* `GetRandomNumber(minimum, maximum)`
* `GetRandomNumbers(count)`
* `GetRandomNumbersAsXml(count)`
* `GetRandomString(count)`

This table show some sample output from these methods:

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
		<td>
			<var>format</var> is optional and can be either of 'd' (default), 'n', 'p', 'b', or 'x'
		</td>
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


### GetRandomGuid()

The optional format string yields the following types of GUIDs:

<table>
	<tr><td>d</td><td><code>2defabe0-0968-43f5-9486-ccef26d77a46</code></td></tr>
	<tr><td>n</td><td><code>d9565077f54f4b9688b854076d004579</code></td></tr>
	<tr><td>p</td><td><code>(27461e8e-82df-44d5-8585-9cb287f68284)</code></td></tr>
	<tr><td>b</td><td><code>{2b40b243-255c-4575-91b2-0466cdf82e13}</code></td></tr>
	<tr><td>x</td><td><code>{0x356bc45d,0xad00,0x48ca,{0xa9,0x6d,0xd5,0x00,0x89,0x34,0xe9,0xc7}}</code></td></tr>
</table>
