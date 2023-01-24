@docArgs()
```
"title": ".emdd | Home", 
"links": ["./style.css"]
```

@weave(name="page_header")
```
"title": "Extensible Markdown (.emdd)", 
"lead": "A format for writing web documents, somewhere in-between Markdown and your typical HTML, CSS and JS." 
```

Extensible Markdown Documents (emdd) is an extension to Markdown for writing web documents, which can then be transpiled with the use of plugins to your desired output, or lack of. This allows Markdown to remain relatively as normal while also promoting extensibility. By default, `md` files will have their Markdown content parsed and output as HTML. Blocks annotated with an `@` specifier will be processed via pre-processing and content processing plugins where supported.

> The API for Extensible Markdown will be classed as unstable until a version 1 release is reached

## The reasoning behind Extensible Markdown

Markdown serves the developer community quite kindly, offering a simple and fast way of writing prose. The major problem to this is when you want something a bit more in your Markdown, this is the reason for creating this project.

If you like this project, feel free to use it as you please.

If you would like to contribute to Extensible Markdown, please visit the GitHub repository for this page and submit a pull request with your contribution (contribution guidelines do not currently exist).

## Example document

The following is an example of an emdd document:

@lit()
```
<pre><code>@docArgs()
\```
"title": "Example page"
\```

# Title

Some paragraph text. Some paragraph text. Some paragraph text. Some paragraph text. Some paragraph text. Some paragraph text. Some paragraph text. 
Some paragraph text. Some paragraph text. Some paragraph text. Some paragraph text. Some paragraph text. Some paragraph text. 
Some paragraph text. Some paragraph text. Some paragraph text.

@js()
\```
let sum = 3 + 3;
return `<p>Sum of 3 + 3 is ${sum}</p>`;
\```
</pre></code>
```

After transpilation to HTML, the contents of the document would roughly look as follows:

```html
<html>
    <head>
        <title>Example page</title>
    </head>
    <body>

        <h1>Title</h1>
        <p>
            Some paragraph text. Some paragraph text. Some paragraph text. Some paragraph text. Some paragraph text. Some paragraph text. Some paragraph text.
            Some paragraph text. Some paragraph text. Some paragraph text. Some paragraph text. Some paragraph text. Some paragraph text.
            Some paragraph text. Some paragraph text. Some paragraph text.
        </p>

        <p>Sum of 3 + 3 is 6</p>
    </body>
</html>
```