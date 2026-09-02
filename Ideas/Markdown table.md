---
cssclasses:
  - table-valign-center
---
The exact cell widths can vary. You need at least 3 dashes (`---`) per header column.
```tx
| Markdown | Result |
| --- | --- |
| <code>\| Header 1 \| Header 2 \|<br>\| -------- \| -------- \|<br>\| Item 1   \| Item 2   \|<br>\| Item 3   \| Item 4   \|</code> | <table><tr><th>Header 1</th><th>Header 2</th></tr><tr><td>Item 1</td><td>Item 2</td></tr><tr><td>Item 3</td><td>Item 4</td></tr></table> |
| <code>\| Left al \| Centre al \| Right al \|<br>\| :------ \| :-------: \| -------: \|<br>\| Left    \|  Centre   \|    Right \|</code> | <table><tr><th>Left al</th><th align="center">Centre al</th><th align="right">Right al</th></tr><tr><td>Left</td><td align="center">Centre</td><td align="right">Right</td></tr></table> |
```
Within tables you can add **styling**, **code**, **code blocks** or **links**, but no **headings**, **blockquotes**, **lists**, **images** or most **HTML tags**.
You can display a `|` (pipe) character in tables using `&#124;`.