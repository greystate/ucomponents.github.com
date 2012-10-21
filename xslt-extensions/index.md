---
layout: default
title: XSLT Extensions
category: root
---

<div class="page-header">
  <h1>XSLT Extensions</h1>
</div>



## Enabling XSLT extensions for use in your XSLT templates.

To use the uComponents XSLT extensions in your XSLT templates, you'll first need to make sure that
the particular extension has been registered. You will also need to manually register the extension
in any XSLT files you've created prior to installing uComponents.

You'll need to find the `xsltExtensions.config` file in the `config` directory, and check for the
existence of an `<ext>` element referring to the particular extension. For example, if you need to
use a method in the [Random](random) extension, your `~/config/xsltExtensions.config` file should contain
the following:

<pre><code>&lt;XsltExtensions&gt;
	...
	&lt;ext assembly=&quot;uComponents.Core&quot; type=&quot;<strong>uComponents.Core.XsltExtensions.Random</strong>&quot; alias=&quot;<strong>ucomponents.random</strong>&quot; /&gt;
	...
&lt;/XsltExtensions&gt;</code></pre>

Also, in the XSLT files where you'll be using the extension, you'll need to declare a prefix for use with the extension.
This is done with a namespace declaration on the <code>&lt;xsl:stylesheet&gt;</code> element (you can use any prefix you like
but it's very common to reuse the alias from the config file. Furthermore, you need to add the prefix to
the list prefixes to exclude from the generated output.

<pre><code>&lt;xsl:stylesheet version=&quot;1.0&quot;
	...
	xmlns:<strong>ucomponents.random</strong>=&quot;<strong>urn:ucomponents.random</strong>&quot;
	...
	exclude-result-prefixes=&quot;... <strong>ucomponents.random</strong>&quot;&gt;
	...
&lt;/xsl:stylesheet&gt;
</code></pre>

All of this is done automatically for you, if you choose to enable the XSLT extensions on the final screen, when installing
uComponents. After enabling the extensions, they'll be registered in the config file, and every XSLT file created in Umbraco
will have all the namespace declarations needed.
