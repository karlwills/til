# Use the `@each` directive to perform tasks to a number of items in a `list` or `map`

The `@each` directive allows you to loop over a provided `list` or `map` in Sass, giving you the flexibility to dynamically add styles where needed.

This is a good alternative approach to manually adding a number of repatitive styles to different classes.

**Note**: When concatenating variables within a string, or using a it as a class/element, the variable will need to be preceeded with `#{` and prepended with `}` which allows the compiler to recognise that is it a variable.

```scss
$tiles: (
    pastoral: $colour-background-tile-pastoral,
    calendar: $colour-background-tile-calendar,
    busy-bees: $colour-background-tile-busy-bees,
    news: $colour-background-tile-news,
    curriculum: $colour-background-tile-curriculum,
    first-school: $colour-background-tile-first-school,
    children: $colour-background-tile-children,
    parents: $colour-background-tile-parents
);

@each $tile, $colour in $tiles {
    .c-tiles__tile--#{$tile} {
        .c-tiles__tile-title {
            background-color: $colour;
        }
    }
}
```

#### Output

```css
.c-tiles__tile--pastoral {
    .c-tiles__tile-title {
        background-color: #d90f5a;
    }
}
```
