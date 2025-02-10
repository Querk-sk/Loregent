---
{"dg-publish":true,"permalink":"/loregent/assets/fleeting-notes/obsidian-callouts/","noteIcon":""}
---


#### Callouts

Use callouts to include additional content without breaking the flow of your notes.

To create a callout, add `[!info]` to the first line of a blockquote, where `info` is the _type identifier_. The type identifier determines how the callout looks and feels. To see all available types, refer to [Supported types](https://help.obsidian.md/Editing+and+formatting/Callouts#Supported%20types).

```markdown
> [!info]
> Here's a callout block.
> It supports **Markdown**, [[Internal link|Wikilinks]], and [[Embed files|embeds]]!
> ![[Engelbart.jpg]]
```

>[!Info]
>
Here's a callout block.  
It supports **Markdown**, [Wikilinks](https://help.obsidian.md/Linking+notes+and+files/Internal+links) and [embeds](https://help.obsidian.md/Linking+notes+and+files/Embed+files)!  
![Engelbart.jpg](https://publish-01.obsidian.md/access/f786db9fac45774fa4f0d8112e232d67/Attachments/Engelbart.jpg)

Callouts are also supported natively on [Obsidian Publish](https://help.obsidian.md/Obsidian+Publish/Introduction+to+Obsidian+Publish).

>[!Note]
>
If you're also using the Admonitions plugin, you should update it to at least version 8.0.0 to avoid problems with the new callout feature.

##### Change the title

By default, the title of the callout is its type identifier in title case. You can change it by adding text after the type identifier:

```markdown
> [!tip] Callouts can have custom titles
> Like this one.
```

> [!tip] Callouts can have custom titles
> Like this one.

You can even omit the body to create title-only callouts:

```markdown
> [!tip] Title-only callout
```

> [!tip] Title-only callout

### Foldable callouts

You can make a callout foldable by adding a plus (+) or a minus (-) directly after the type identifier.

A plus sign expands the callout by default, and a minus sign collapses it instead.

```markdown
> [!faq]- Are callouts foldable?
> Yes! In a foldable callout, the contents are hidden when the callout is collapsed.
```

> [!faq]- Are callouts foldable?
> Yes! In a foldable callout, the contents are hidden when the callout is collapsed.

### Nested callouts

You can nest callouts in multiple levels.

```markdown
> [!question] Can callouts be nested?
> > [!todo] Yes!, they can.
> > > [!example]  You can even use multiple layers of nesting.
```

> [!question] Can callouts be nested?
> > [!todo] Yes!, they can.
> > > [!example]  You can even use multiple layers of nesting.

### Customize callouts

[CSS snippets](https://help.obsidian.md/Extending+Obsidian/CSS+snippets) and [Community plugins](https://help.obsidian.md/Extending+Obsidian/Community+plugins) can define custom callouts, or even overwrite the default configuration.

To define a custom callout, create the following CSS block:

```css
.callout[data-callout="custom-question-type"] {
    --callout-color: 0, 0, 0;
    --callout-icon: lucide-alert-circle;
}
```

The value of the `data-callout` attribute is the type identifier you want to use, for example `[!custom-question-type]`.

- `--callout-color` defines the background color using numbers (0–255) for red, green, and blue.
- `--callout-icon` can be an icon ID from [lucide.dev](https://lucide.dev/), or an SVG element.

>[!warning] Note about lucide icon versions
>
Obsidian updates Lucide icons periodically. The current version included is shown below; use these or earlier icons in custom callouts.  
>
Version `0.268.0`  
ISC License  
Copyright (c) 2020, Lucide Contributors

>[!tip] SVG icons
>
Instead of using a Lucide icon, you can also use a SVG element as the callout icon.

```css
--callout-icon: '<svg>...custom svg...</svg>';
```

##### Supported types

You can use several callout types and aliases. Each type comes with a different background color and icon.

To use these default styles, replace `info` in the examples with any of these types, such as `[!tip]` or `[!warning]`.

Unless you [Customize callouts](https://help.obsidian.md/Editing+and+formatting/Callouts#Customize%20callouts), any unsupported type defaults to the `note` type. The type identifier is case-insensitive.

Note

```md
> [!note]
> Lorem ipsum dolor sit amet
```

> [!abstract] 
> Lorem ipsum dolor sit amet
>

---

Info

---

Todo

---

Tip

Aliases: `hint`, `important`

---

Success

Aliases: `check`, `done`

---

Question

Aliases: `help`, `faq`

---

Warning

Aliases: `caution`, `attention`

---

Failure

Aliases: `fail`, `missing`

---

Danger

Alias: `error`

---

Bug

---

Example

---

Quote

Alias: `cite`
#### Link
- https://help.obsidian.md/Editing+and+formatting/Callouts
- [[Obsidian - Link\|Obsidian - Link]] , [[návod - link\|návod - link]]