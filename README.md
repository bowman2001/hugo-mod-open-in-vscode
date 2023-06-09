# hugo-mod-open-in-vscode

The module contains two partials, which can be placed before and after any HTML element in your templates which does **not contain a link**. 

## Prerequisites

- A local Hugo project 

- A local vscode installation

## Function

If the local Hugo project is rendered **in server-mode**, the two partials wrap a link around the HTML element. The link starts with `vscode://file` and then follows the full path to the current content file. In Hugo’s production mode, these partials do nothing.

## Security consideration

If and only if Hugo’s server-mode is configured to show the preview under a public IP address (by default it shows only on localhost), the full path to the project is visible in the link. Which may be a security concern.  
