# hugo-mod-open-in

The module contains two partials, which can be placed before and after any HTML element in your templates that doesn't contain a link already.

## Prerequisites

- A local Hugo project

- A local VSCode or VSCodium installation

## Function

If the local Hugo project is rendered **in server-mode**, the two partials wrap a link around the HTML element. The link starts with `vscode://file` followed by the full path to the current content file (if it is available). In production mode, the partials don’t generate anything.

In case you would like to use VSCodium you need to reconfigure the name and the protocol in your parameter section:

```yaml
params:
  modOpenIn:
    name: VSCodium
    protocol: vscodium
```

## Security consideration

If and only if Hugo’s server-mode is configured to show the preview under a public IP address (by default it shows only on localhost), the full path to the project is visible in the link. Which may be a security concern.
