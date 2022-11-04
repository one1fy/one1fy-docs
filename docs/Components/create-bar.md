---
sidebar_position: 2
---

# Create Bar

Bar is **a form of organizing UI components** which can be used for:

- **laying out multiple components**
- **dividing and organizing content**
- **dynamic spacing**

## Create your first Bar

Create a bar in `orchestrator` following `components`:

Initialize the bar component using these parameters

```md title="components"
pub struct BarContainer {
    pub id: Uuid,
    pub on_load: Option<fn()>,
    pub visible: bool,
    pub height: u32,
    pub width: u32,
    pub left: u32,
    pub top: u32,
    pub children: Vec<Box<dyn ComponentTraits>>,
    pub orientation: Orientation,
    pub remaining_x: u32,
    pub remaining_y: u32,
}
```

## Style the Bar

You can easily style and edit the bar using the parameters. For example:

```
BarContainer {
    id: Uuid::new_v4(),
    on_load: on_load,
    visible: visible,
    height: height,
    width: width,
    left: left,
    top: top,
    children: x,
    orientation: orientation,
    remaining_x: width,
    remaining_y: height,
}

impl GetHeight for BarContainer {
    fn get_height(&self) -> u32 {
        self.height
    }
}

impl GetWidth for BarContainer {
    fn get_width(&self) -> u32 {
        self.width
    }
}

impl SetLeft for BarContainer {
    fn set_left(&mut self, value: u32) {
        self.left = value;
    }
}

impl SetTop for BarContainer {
    fn set_top(&mut self, value: u32) {
        self.top = value;
    }
}

impl Draw for BarContainer{
    fn draw(&self, canvas: &mut Canvas) {
        if self.visible {
            for child in self.children.iter() {
                child.draw(canvas);
            }
        }
    }
}
```


