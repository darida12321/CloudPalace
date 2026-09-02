---
cssclasses:
  - table-valign-center
---
This [[Obsidian]] plugin extends the default [[Markdown table|table]] syntax using [[MultiMarkdown|MultiMarkdown]]'s table, with extra features. You can create these tables by using a `-tx-` prefix, or a ```` ```tx```` [[Markdown code block|code block]].

````
```tx
|             |          Grouping           || 
First Header  | Second Header | Third Header | 
 ------------ | :-----------: | -----------: | 
Content       |          *Long Cell*        || 
^^            |   **Cell**    |         Cell | 
New section   |     More      |         Data | 
And more      | With an escaped '\|'        || 
```
````
```tx
|             |          Grouping           || 
First Header  | Second Header | Third Header | 
 ------------ | :-----------: | -----------: | 
Content       |          *Long Cell*        || 
^^            |   **Cell**    |         Cell | 
New section   |     More      |         Data | 
And more      | With an escaped '\|'       || 
```

##### Extra features:
Some extra features over [[MultiMarkdown|MultiMarkdown]]'s tables are:
- Cells can be **merged vertically** using `^^`.
- Tables can be **headless** if you don't define the head.
- Rows can be merged using a `\`.


---
Use this [[CSS]] snippet in [[Obsidian]] to add vertical alignment:
```
---
cssclasses:
  - table-valign-center
---
```


