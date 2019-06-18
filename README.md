`highlight.js` syntax definition for GraphQL.

For more about highlight.js, see https://highlightjs.org/

For more about GraphQL, see https://graphql.org/

### Usage

Simply include the `highlight.js` script package in your webpage or node app, load up this module and apply it to `hljs`.

If you're not using a build system and just want to embed this in your webpage:

```html
<script type="text/javascript" src="/path/to/highlight.pack.js"></script>
<script
  type="text/javascript"
  src="/path/to/highlightjs-graphql/graphql.js"
></script>
<script type="text/javascript">
  hljs.registerLanguage("graphql", window.hljsDefineGraphQL);
  hljs.initHighlightingOnLoad();
</script>
```

If you're using webpack / rollup / browserify / node:

```javascript
var hljs = require("highlightjs");
var hljsDefineGraphQL = require("highlightjs-graphql");

hljsDefineGraphQL(hljs);
hljs.initHighlightingOnLoad();
```
