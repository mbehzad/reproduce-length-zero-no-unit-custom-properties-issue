# Minimal Reproducing Repo for stylelint-config-standard's `length-zero-no-unit` setup in combination with custom properties

SCSS code:

```scss
.element {
  --offset: 0px;

  left: calc(var(--offset) + 50%);
}
```

stylelintrc config:

```json
{
  "extends": "stylelint-config-standard"
}
```

Error:
```
2:14  ✖  Unexpected unit  length-zero-no-unit
```

Where `left: calc(var(--offset) + 50%);` with `--offset: 0px` results to invalid `left: calc(0 + 50%);`

Run `npm test` to see the stlyint error.
