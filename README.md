# transloco-extract-duplicate-keys
Demonstration repo for transloco extract duplicate keys bug.

Running `i18n:find` discovers 4 missing keys, but we expect 2.
Running `i18n:extract` populates `en.json` with
```json
{
  "nested.comment1": "Missing value for 'nested.comment1'",
  "nested.comment2": "Missing value for 'nested.comment2'",
  "comment1": "Missing value for 'comment1'",
  "comment2": "Missing value for 'comment2'"
}
```
instead of the expected
```json
{
  "nested.comment1": "Missing value for 'nested.comment1'",
  "nested.comment2": "Missing value for 'nested.comment2'",
}
```

## Versions
* `@ngneat/transloco`: 2.18.3
* `@ngneat/transloco-keys-manager`: 2.2.1
* Angular: 10.0.5