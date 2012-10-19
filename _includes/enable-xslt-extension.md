## Enabling the XSLT extension for use in your XSLT templates.

Add the following XML snippet to your `~/config/xsltExtensions.config` file:

	<XsltExtensions>
		...
		<ext assembly="{{ page.extassembly }}" type="{{ page.exttype }}" alias="{{ page.extalias }}" />
		...
	</XsltExtensions>

In case you've already created some XSLT files in Umbraco that you want to use this extension in, you'll likely need
to assign a prefix using a namespace declaration, and exclude the prefix from any output:

	<xsl:stylesheet version="1.0"
		...
		xmlns:ucom.random="urn:{{ page.extalias }}"
		...
		exclude-result-prefixes="... {{ page.extprefix }}">
		...
	</xsl:stylesheet>