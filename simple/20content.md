# A few easy steps

1. Use `gitshow init` to create an empty presentation.
2. Edit the markdown content. Use `gitshow serve` to watch the result live.
3. Maintain the presentation in a git repo.

---

# Configuration

The presentation config is in `presentation.json`.

```json
{
    "id": "presentation",
    "title": "Sample Presentation",
    "author": "Radek Burget",
    "lang": "en",
    "template": {
        "name": "default",
        "properties": {
            "theme": "moon",
            "highlight": "googlecode"
        }
    },
    "reveal": {
        "center": true,
        "hash": true
    },
    "contents": [
        "10intro.md",
        "20content.md",
        "99final.md"
    ]
}
```

We are using the `moon` theme now. Any [Reveal.js theme](https://revealjs.com/themes/) can be used.

---

# Content

The text can be split to any number of markdown files. Add them to the `contents` section in the config.

Images and other assets live in the `assets` folder.

![Square](assets/square.svg) <!-- .element: class="r-stretch" title="An SVG image" -->

`![Square](assets/square.svg)`

---

# Math formulas

`$$ MI(U,V)=\sum_{i=1}^{|U|} \sum_{j=1}^{|V|} \frac{|U_i\cap V_j|}{N}\log\frac{N|U_i \cap V_j|}{|U_i||V_j|} $$`

---

# Templates

**GitShow** offers a few basic templates:

- The [simple template](https://github.com/gitshow-js/demos/tree/main/simple) (*you are seeing just now*) -- it simply uses a built-in Reveal.js theme.
- The [classic template](https://github.com/gitshow-js/demos/tree/main/classic) -- a "classical" slide layout with header and footer. See the [live demo](https://gitshow.net/gh/gitshow-js/demos@main/classic) for details.

The template definition is stored in the `template` folder and you can customize it arbitrarily.

---

# Show it online

When you share your presentation in a public GitHub repository, it can be directly displayed using the \
[GitShow Viewer App](https://gitshow.net).
