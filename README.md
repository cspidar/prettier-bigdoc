# prettier-bigdoc

Modified Prettier for large-scale documentation task. Based on Prettier version `3.3.3`. Supports for **md**, **mdx**.

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

1. Add plugin in overrides field.
   ```bash
   npm pkg set overrides.${PLUGIN_NAME}.prettier="npm:prettier-bigdoc"
   ```
1. Install plugin.
   ```bash
   npm install --save-dev prettier ${PLUGIN_NAME}
   ```

## Modified features

### Table hyphen limitation

Fix hyphen of table to 3 to allow reading and editing large-scale table with word wrap applied. Make the worst a little less worst.

```md
<!-- prettier 3.3.3 -->
| Long and complicated header 1                                                                                                                     | Long and complicated header 2                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| The first long and complicated descriptions and text to supplement them.<br>Less important descriptions that should be placed on the bottom line. | Second long and complicated descriptions and text to supplement them.<br>Less important descriptions that should be placed on the bottom line. |

<!-- prettier-bigdoc -->
| Long and complicated header 1 | Long and complicated header 2 |
| --- | --- |
| The first long and complicated descriptions and text to supplement them.<br>Less important descriptions that should be placed on the bottom line. | Second long and complicated descriptions and text to supplement them.<br>Less important descriptions that should be placed on the bottom line. |
```

### `<br>` tags auto closure 

```md
<!-- prettier 3.3.3 -->
<br>

<!-- prettier-bigdoc -->
<br />
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
