CSS3MultiColumn
===============

An update to CSS3MultiColumn by Cédric Savarese to support HTML5 elements.

The original code can be found here:
http://www.csscripting.com/css-multi-column/


Usage

Upload the script to your site.
Attach the script after the links to your stylesheet(s). Example:

    <link rel="stylesheet" type="text/css" href="stylesheet.css" />
    <script type="text/javascript" src="css3-multi-column.js"></script>

You can now use any of these CSS3 multi-column properties in your stylesheet (providing that you understand the limitations given below).

    New CSS Property 	Type 	Example
    column-count 	a number 	3
    column-width 	a value in pixels 	200px
    column-gap 	a value in pixels 	10px
    column-rule 	a border definition 	1px solid #000

Limitations (as of version 1.0beta)

Values for column-width and column-gap must be given in pixels. You must include column-count and use long-hand syntax.
The implementation relies on a light javascript css parsers. Avoid complex css structures (like cascading rules).

This is ok:

    .article {
       column-count: 3;
       column-gap: 20px;
    }

    This is likely to break:
    #somearticleid {
        column-count: 3;
    }
    .different_selector {
        column-gap: 20px;
    }
Also, for now the parser still processes commented rules (likely to be fixed soon) .
The parser only processes linked stylesheets (link tag). Style elements, import directives and inline styles are ignored.
Be aware that the markup of your page is modified by the javascript, so it is possible that some CSS rules may not work after the multi-column layout is applied.
