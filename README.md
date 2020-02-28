# pdf_find_replace
Find and replace a string in a pdf document


## Usage

```shel
$ ./pdf_find_replace <input-file> <find> [<replace> <output-file>]
```

`<input-file>` should be a pdf.
`<find>` a string and `<replace>` it by another string (by default empty).
`<output-file>` is by default `mod_<input-file>`

Notes:
* sed expression is defined as `sed -E -e r|<find>|<replace>|g` as such that delimeter `|` cannot be used in `<find>` and `<replace>` strings.
* `<input-file>` is first uncompressed using `pdftk` (and re-compressed generating the `<output-file>`)
