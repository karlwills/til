# Imports and Exports


## imports

The `import` statement is used to import bindings that have been previously exported by another module.

#### Import Examples

```javascript
import exportName from "your-module";            // will import a 'default' export from "your-module"
import * as moduleName from "your-module";       // will insert "moduleName" into the current scope, along with all the exports within it
import { singleExport } from "your-module";      // will import a single 'named' export from "your-module"
import { singleExport, andotherExport } from "your-module";          // will import both 'singleExport' and 'anotherExport' from "your-module"
import { reallyLongExportName as shortName } from "your-module";     // will rename the exported name as something else when importing
```

#### Dynamic Imports

You can use the `import` keyword as a function to dynamically import a module. This will return a promise.

```javascript
import('./path/to/module.js').then((returnedModule) => {
    // Do whatever you need to do.
});
```

You can also use `await` with this implementation

```javascript
let module = await import('./path/to/module.js');
```

## Exports

The `export` statement is used when creating JavaScript modules to export bindings (functions, objects, or [primitive values](https://developer.mozilla.org/en-US/docs/Glossary/Primitive)) so they can be used in by other modules using the `import` statement.

There are 3 types of exports:
* Named exports (0 or more per module)
* Default exports (*one* per module)
* Hybrid exports

#### Export Examples

```javascript
// Named exports
export { aFunction, aVariable };     // export features that were declared earlier

// export individual features (functions, let, const etc.)
export let myVariable = 200;
export function myCoolFunc() { ... };

// Default exports
export { myCoolFeature as default };    // export a feature that was declared earlier as a default
export default function myCoolFunc() { ... };
export default componentName;
```

*Note:* It is mandatory when importing a *named* export to use the name that it was exported with. However, another name can be used when importing a *default* export from another module.

#### Browser Compatibility
Both `import` and `export` has support in all modern browsers, with no support in Internet Explorer.

#### More Information
[MDN - Import](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import)
[MDN - Export](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export)
