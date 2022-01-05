#  Svelte Language Server Yarn PnP resolution crash PoC

```
[snip]\svelte-language-server-pnp-crash\.pnp.cjs:11508
    throw firstError;
    ^

Error: svelte-language-server tried to access vscode-languageserver-protocol, but it isn't declared in its dependencies; this makes the require call ambiguous and unsound.

Required package: vscode-languageserver-protocol
Required by: svelte-language-server@npm:0.14.16 (via [snip]\svelte-language-server-pnp-crash\.yarn\cache\svelte-language-server-npm-0.14.16-ad271df40a-4826ff5df6.zip\node_modules\svelte-language-server\dist\src\plugins\typescript\features\)

Require stack:
- [snip]\svelte-language-server-pnp-crash\.yarn\cache\svelte-language-server-npm-0.14.16-ad271df40a-4826ff5df6.zip\node_modules\svelte-language-server\dist\src\plugins\typescript\features\ImplementationProvider.js
- [snip]\svelte-language-server-pnp-crash\.yarn\cache\svelte-language-server-npm-0.14.16-ad271df40a-4826ff5df6.zip\node_modules\svelte-language-server\dist\src\plugins\typescript\TypeScriptPlugin.js
- [snip]\svelte-language-server-pnp-crash\.yarn\cache\svelte-language-server-npm-0.14.16-ad271df40a-4826ff5df6.zip\node_modules\svelte-language-server\dist\src\plugins\index.js
- [snip]\svelte-language-server-pnp-crash\.yarn\cache\svelte-language-server-npm-0.14.16-ad271df40a-4826ff5df6.zip\node_modules\svelte-language-server\dist\src\server.js
- [snip]\svelte-language-server-pnp-crash\.yarn\cache\svelte-language-server-npm-0.14.16-ad271df40a-4826ff5df6.zip\node_modules\svelte-language-server\bin\server.js
- [snip]\svelte-language-server-pnp-crash\.pnp.cjs
    at Function.external_module_.Module._resolveFilename ([snip]\svelte-language-server-pnp-crash\.pnp.cjs:11507:55)
    at Function.external_module_.Module._load ([snip]\svelte-language-server-pnp-crash\.pnp.cjs:11306:48)
    at Module.require (internal/modules/cjs/loader.js:1006:19)
    at require (internal/modules/cjs/helpers.js:88:18)
    at Object.<anonymous> ([snip]\svelte-language-server-pnp-crash\.yarn\cache\svelte-language-server-npm-0.14.16-ad271df40a-4826ff5df6.zip\node_modules\svelte-language-server\dist\src\plugins\typescript\features\ImplementationProvider.js:4:42)
    at Module._compile (internal/modules/cjs/loader.js:1125:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1155:10)
    at Module.load (internal/modules/cjs/loader.js:982:32)
    at Function.external_module_.Module._load ([snip]\svelte-language-server-pnp-crash\.pnp.cjs:11356:14)
    at Module.require (internal/modules/cjs/loader.js:1006:19)
[Error - 8:19:27 PM] Connection to server got closed. Server will not be restarted.
```
