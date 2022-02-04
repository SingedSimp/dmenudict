This is my fork of https://github.com/madprops/rofidict (which is a fork of https://github.com/defCoding/rofi-dictionary) with is modified to run on dmenu instead of rofi.

You will need to set your font manually in the config.json file, but the default is JetBrainsMono, so if you already have it installed you should be fine.

It also requires xclip, but that can be removed by changing config.json

You will need to create a JSON file named `creds.json` in the cloned repo. This will contain the `app_key` and `app_id` needed for the Oxford Dictionary API. To retrieve your values, create an account and application at the [OxfordDictionary website](https://developer.oxforddictionaries.com/). Once you've created your application, get your `app_key` and `app_id` from the API Credentials page.

```json
{
  "app_key": "APP KEY GOES HERE",
  "app_id": "APP ID GOES HERE"
}
```

It's necessary to provide the language code as an argument:

`/path/to/dmenudict.py en` 

(For english definitions)

`/path/to/dmenudict.py es` 

(For spanish definitions)

[Check available languages here](https://developer.oxforddictionaries.com/documentation/languages)

Selecting a definition copies it to the clipboard if `xclip` is installed.
