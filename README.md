# Modern CSS

A small demo page that shows off newer CSS features — no JavaScript, no build step, just HTML and CSS. It goes with the `Modern CSS.pptx` presentation.

## How it works

`index.html` has one `<section>` per feature, and each feature has its own stylesheet in `css/`. Only one section is shown at a time. Which one is controlled by a single custom property in `css/main.css`:

```css
:root {
  --step: "variables";
}
```

Each section uses the CSS `if()` function to show itself only when `--step` matches its name:

```css
.nesting {
  display: if(style(--step: "nesting"): grid; else: none);
}
```

To move to the next demo, change `--step` to another name from the list below.

## The demos

| Step           | File               | What it shows                                                      |
| -------------- | ------------------ | ------------------------------------------------------------------ |
| `variables`    | `variables.css`    | Custom properties, `@property`, and theme colors                   |
| `nesting`      | `nesting.css`      | Native CSS nesting with `&`                                        |
| `progress`     | `progress.css`     | `progress()` for fluid font size and spacing                       |
| `has`          | `has.css`          | The `:has()` parent selector (click the cockatoo)                  |
| `anchor`       | `anchor.css`       | Anchor positioning (`position-anchor`, `anchor()`)                 |
| `scope`        | `scope.css`        | `@scope` to limit where styles apply                               |
| `color`        | `color.css`        | `oklch()`, `color-mix()`, and `color-scheme` light/dark switching  |
| `field-sizing` | `field-sizing.css` | Inputs and textareas that grow with their content                  |
| `container`    | `container.css`    | Container queries (resize the box to see the layout change)        |
| `grid`         | `grid.css`         | Named grid lines for full-bleed and content-width layouts          |

## Running it

Open `index.html` in a browser. Use an up-to-date Chromium-based browser (Chrome or Edge), since some of these features — like `if()`, `progress()` and anchor positioning — are very new and not supported everywhere yet.
