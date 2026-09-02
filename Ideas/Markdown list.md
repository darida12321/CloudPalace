---
cssclasses:
  - table-valign-center
---
**Ordered lists** don't care about the numbers used. 
**Unordered lists** can use allowed symbols in any combination.
```tx
| Markdown | Result | 
| --- | --- |
|    1. List 1    | <ol><li>List1</li><li>List2<ol><li>List3</li></ol></li></ol> | \
|    18. List 2    | | \
|      0. List 3 | | 
|    - List 1 | <ul><li>List1</li><li>List2<ul><li>List3</li></ul></li></ul> | \
|    * List 2 | | \
|      + List 3 | |
```
