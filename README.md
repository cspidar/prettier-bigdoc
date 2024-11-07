# prettier-bigdoc

Modified Prettier for large-scale documentation task. Based on Prettier version `3.3.3`. Supports for md, mdx.

## Prettier?

About Prettier, see below.

- Web: https://prettier.io/
- GitHub: https://github.com/prettier/prettier

## Install

```bash
npm install --save-dev prettier@npm:prettier-bigdoc
```

### If you want install plugin

You can use plugins that are supported by Prettier version 3.3.3.

```bash
npm install --save-dev prettier @prettier/plugin-xml  --legacy-peer-deps
```

## Modified features

### Table hyphen limitation

Fix hyphen of table to 3 to allow reading and editing large-scale table with word wrap applied. Make the worst a little less worst.

```md
<!-- Prettier -->
| Long and complicated header 1                                                                                                                     | Long and complicated header 2                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| The first long and complicated descriptions and text to supplement them.<br>Less important descriptions that should be placed on the bottom line. | Second long and complicated descriptions and text to supplement them.<br>Less important descriptions that should be placed on the bottom line. |

<!-- Prettier-bigdoc -->
| Long and complicated header 1 | Long and complicated header 2 |
| --- | --- |
| The first long and complicated descriptions and text to supplement them.<br>Less important descriptions that should be placed on the bottom line. | Second long and complicated descriptions and text to supplement them.<br>Less important descriptions that should be placed on the bottom line. |
```




### More will be added as needed

In future.

---

## Dev commands

### Build

```
npm run build
```

### Test

#### Project

```
node ./bin/prettier.cjs --write proto-test/example.md
```

#### Dist

```
node ./dist/bin/prettier.cjs --write proto-test/example.md
```

---

## TODO

- [x] `<br>` -> `<br />`
- [ ] Update test case of markdown table
- [ ] Add more features
