---
sidebar_position: 4
---

# Create Checkbox

Checkbox is **a form of interactivity** which can be used for:

- **providing boolean interactivity**
- **dynamically representing boolean values**

## Create your first Checkbox

Create a checkbox in `orchestrator` following `components`:

Initialize the checkbox component using these parameters

```md title="components"
pub struct CheckBox {
    pub id: Uuid,
    pub left: u32,
    pub top: u32,
    pub height: u32,
    pub width: u32,
    pub visible: bool,
    pub componentType: Type,
    pub checkType: CheckType,
    pub checked: bool,
    pub text: String,
    pub altText: Option<String>,
}
```

## Style the Checkbox

You can easily style and edit the checkbox using the parameters. For example:

```
let cbox: CheckBox = CheckBox::new(
    0,
    0,
    33,
    100,
    true,
    CheckType::BOX,
    false,
    "One1fy is awesome".to_string(),
    Some("One1fy is really awesome".to_string()),
);
```


