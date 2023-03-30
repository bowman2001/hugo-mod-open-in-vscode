# hugo-mod-open-in-vscode

The module contains two partials, which can be placed before and after any HTML element in your templates which does **not contain a link**. 

## Prerequisites

- A local Hugo project 

- A local vscode installation

## Function

If the local Hugo project is rendered **in server-mode**, the two partials wrap a link around the HTML element. The link starts with `vscode:\\` and contains the full path to the current content file. To produce the path the partial needs the parameter `sourcePath` in the configuration. It needs to contain the full path to your local content folder. Without this parameter, nothing happens.

## Security Risk!

To include the path to your local project in a public configuration file may be a security risk. Hugo allows to separate the local development configuration from the production configuration, if this a concern. And you should separate this parameter, then, and exclude it from version control. 
