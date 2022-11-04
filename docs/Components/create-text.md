---
sidebar_position: 3
---

# Create Text

Text is **a form of implementing text** which can be used for:

- **displaying pure text**
- **adding text to components**
- **dynamic content representation**

## Create your first Text

Create a box in `orchestrator` following `components`:

Initialize the text component using these parameters

```md title="components"
pub struct TextComponent {
    pub left: u32,
    pub top: u32,
    pub font_size: u32,
    pub text: String,
    pub color: crate::components::Color,
}
```

## Style the text

You can easily style and edit the text using the parameters. For example:

```
use skia_safe::{Font, FontStyle};

let typeface: Option<Typeface> = Typeface::new(
    "Times New Roman",
    FontStyle::new(
        Weight::NORMAL,
        Width::NORMAL,
        Slant::Upright,
    ),
);

let font: Font = Font::new(
    typeface.unwrap(),
    Some(64.0 as f32),
);

let text: Option<TextBlob> = TextBlob::from_str(
    self.text.as_str(),
    &font,
);

let mut paint: Paint = Paint::new(
    Color4f::new(255.0, 0.0, 0.0, 0.0),
    None
);

paint.set_style(skia_safe::PaintStyle::Fill);
paint.set_color(self.color.color);

canvas.draw_text_blob(
    text.unwrap(),
    Point::new(100.0, 100.0),
    &paint,
);
```


