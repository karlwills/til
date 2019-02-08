# Use the CSS General sibling combinator to toggle a `nav` element

Using a combination of the CSS general sibling combinator `~` and a HMTL label and checkbox, you can create a toggle element 
pattern that can be used for things like a mobile navigation show/hide.

#### HTML

```html
<input type="checkbox" name="menu-toggle" class="menu-toggle" id="menu-toggle">
<label for="menu-toggle" class="menu-toggle-label" aria-label="Menu">Menu</label>

<nav role="navigation">
    <a title="Menu Link" href="#">Menu Link</a>
    <a title="Menu Link" href="#">Menu Link</a>
    <a title="Menu Link" href="#">Menu Link</a>
    <a title="Menu Link" href="#">Menu Link</a>
</nav>
```

#### CSS

```css
[role="navigation"] {
   transform: translateX(-100%);
   transition: .2s;
}

.menu-toggle-label {
   cursor: pointer;
}

.menu-toggle {
    display: none;
}

.menu-toggle:checked ~ [role="navigation"] {
    transform: translateX(0);
}
```

Example: [CodePen](https://codepen.io/karlwills/pen/Vgyqym)

#### Further Reading
[MDN - General sibling combinator](https://developer.mozilla.org/en-US/docs/Web/CSS/General_sibling_combinator)
