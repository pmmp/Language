# PocketMine-Language

These files contain translation strings used in PocketMine-MP.

## Contributing translations
To contribute translations, please use the [Crowdin Translation Page](http://translate.pocketmine.net/), select the language you want to translate and and go to PocketMine-MP and select "PocketMine core strings". There may be multiple branches available - if in doubt, stick with `stable`.

## For maintainers
### Adding new strings
Only English should be modified directly. To add new strings, add them ONLY to eng.ini. Crowdin will then synchronize them and the new strings will be put up for translation within Crowdin.

### Versioning
- Versions must be updated in [`tag-patches.yml` workflow](.github/workflows/tag-patches.yml#L19).
- When removing a string, or adding/removing/renaming parameters, bump the major version, e.g. `2.8.0` -> `3.0.0`
- When adding new strings, bump the minor version, e.g. `2.8.0` -> `2.9.0`
- Patches are automatically tagged by GitHub Actions whenever new translations are merged from Crowdin.

### Pitfalls
- If you have issues with translation files being deleted, add a language mapping in the Crowdin config. Some issues arose with Chinese due to Chinese Simplified and Chinese Traditional both mapping to `zho`, requiring a mapping to `zho-cn` for simplified.
