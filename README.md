# abbreviation-discourse-plugin
----------

This plugin translates certain whitelisted words to a HTML `<abbr>` tag. Example: if you register the word IMHO with the title "In My Humble Opinion" it will be automatically translated as `<abbr title="In My Humble Opinion">IMHO</abbr>`

##Features
----------

* Create a list of abbreviations
* Configurable through admin settings
* Option to disable the plugin through the admin settings

##Initial Configuration
----------

Modify the variable `abbreviations_plugin_list` in the file `settings.yml` so it contains couples of abbreviation and meaning separated by a pipe `(|)`. The abbreviation and its meaning must be separated by a colon `(:)` .
 Example:

```yaml
plugins:
  abbreviations_plugin_enabled:
    default: true
    client: true
  abbreviations_plugin_list:
    default: IMHO:In My Honest Opinion|YMMV:Your Mileage May Vary|lol:Laughing Out Loud
    client: true
```
You cannot use colons  `(:)` or pipes `(|)` in the definition of your abbreviations.

