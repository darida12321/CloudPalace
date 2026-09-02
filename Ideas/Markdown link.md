---
cssclasses:
  - table-valign-center
---
You can have a piece of text act as a link to another website. This text can be [[Markdown styles|styled]], or it can even be an [[Markdown image|image]]. You can often link to [[Markdown heading ID|Heading ID-s]].

```tx
| Markdown | Result | 
| --- | --- |
| `<https://https://www.foo.com/>` | <https://www.foo.com> |
| `[Markdown](https://www.markdownguide.org)` | [Markdown](https://www.markdownguide.org) |
| `[Markdown](https://www.markdownguide.org "Hower text")` | [Markdown](https://www.markdownguide.org "Hower text") |
| `*[Markdown](https://www.markdownguide.org)*` | *[Markdown](https://www.markdownguide.org)* |
| `**[Markdown](https://www.markdownguide.org)**` | **[Markdown](https://www.markdownguide.org)** |
| ``[`Markdown`](https://www.markdownguide.org)`` | [`Markdown`](https://www.markdownguide.org) |
|    [![markdown\|50](/Admin/Attachments/Markdown_logo.png)] | [![[Markdown_logo.png\|50]]](https://www.markdownguide.org) | \
|    (https://www.markdownguide.org) | |
```

To make the markdown more readable, reference-style links can be created by
```
[Markdown][1]
[1]: <https://www.markdownguide.org>
```
