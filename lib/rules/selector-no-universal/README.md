# selector-no-universal

Disallow the universal selector.

```css
    * {}
/** ↑
 * This selector */
```

## Options

### `true`

The following patterns are considered violations:

```css
* {}
```

```css
*, .foo {}
```

```css
* > [foo] {}
```

The following patterns are *not* considered violations:

```css
a {}
```

```css
.foo {}
```

```css
[foo] {}
```

```css
#foo {}
```

```css
.bar > #foo {}
```
