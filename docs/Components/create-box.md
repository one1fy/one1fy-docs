---
sidebar_position: 1
---

# Create Box

Box is **a basic form of building UI components** which can be used for:

- foundation for **complex UI components**
- **dividing and organizing content**
- **interactivity using on click**

## Create your first Doc

Create a box in `orchestrator` following `components`:

Initialize the box component using these parameters

```md title="components"
pub struct BoxComponent {
    pub left: u32,
    pub top: u32,
    pub height: u32,
    pub width: u32,
    pub style: Style,
    pub visible: bool,
}
```

## Style the box

You can easily style and edit the box using the parameters. For example:

```
let rect = Rect::new(
    left as f32,
    top as f32,
    right as f32,
    bottom as f32,
);

let mut paint: Paint = Paint::new(
    Color4f::new(0.0, 0.0, 0.0, 0.0),
    None
);

paint.set_color(color);
canvas.draw_rect(rect, &paint);
canvas.restore();
```


