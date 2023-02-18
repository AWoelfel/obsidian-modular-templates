# obsidian-modular-templates
a set of small features to be able to use modular templates in obsidian


# Used Plugins

`obsidian-modular-templates` currently relies on this plugins : 

- tasks https://github.com/obsidian-tasks-group/obsidian-tasks
- dataview https://github.com/blacksmithgu/obsidian-dataview
- templater https://github.com/SilentVoid13/Templater
	- The setting `Template folder location` is set to `_obsidian/_templates`
	- The setting `Automatic jump to cursor` is set to `True`
	- The setting `Trigger Templater on new file creation` is set to `True`


# Directories

## `_houskeeping`
contains a set of Markdown files to manage your current project state

## `_obsidian`
contains the heart and guts of all modular templates

### `_scripts`
is the place to store any user script used by `templater`

### `_templates`
is the place to store any tamplates used by `templater`


# Template mechanics

Any template must consist of at least a a `<name>` and a `<version>`.
After the template was created the instance will be moved to `<name>`

## Default templates
By default any template is designed to have a `<name>` and a `<version>` and consists of `six` parts

1. a template header (stored in `/_obsidian/_templates/template.header`)
2. a data section containing data fields for a Markdown instance (stored in `/_obsidian/_templates/<name>.data`)
3. a separator (stored in `/_obsidian/_templates/template.separator`)
4. a body section containing the main body for Markdown instance (stored in `/_obsidian/_templates/<name>.body`)
5. a separator (stored in `/_obsidian/_templates/template.separator`)
6. a template footer (stored in `/_obsidian/_templates/template.footer`)

### Examples

A example for a default templates is [[yacht]], [[person]]

## Custom templates

Any custom template still needs to define a `<name>` and a `<version>` but specify any template `<parts>`.

### Examples

A examples for a custom templates is [[daily]], [[car]]