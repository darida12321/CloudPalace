MultiMarkdown is a superset of [[Markdown|Markdown]]. It adds the ability to work with complete documents, 

- **Abbreviations**: Use `[>MMD]` in text, then `[>MMD]: MultiMarkdown` at the end
- **Citations**: Use `[p. 23][#Doe:2001]` in text, then `[#Doe:2001]: John Doe. *Book*`.
- **Critic**: Mark edits to a text. `multimarkdown --[accept|reject] foo.txt` to accept them
	- Deletions: `{--deleted text --}`.
	- Additions: `{++added text ++}`.
	- Substitutions: `{~~from~>to~~}`.
	- Highlighting: `{==highlight==}`.
	- Comment: `{>>This is a comment<<}`.
- **Cross-References**: `[Overview][]` takes you to the [[Markdown headings|heading]] named `Overview`.
- **Transclusion**: Include another file in the document `{{other_file.txt}}`.
- **Math**: Use [[LaTeX|LaTeX]] for math expressions `$$\frac{1}{2}$$`.
- **Metadata**: A list of metadata at the top of the document.
- **Smart typography**: Converts `"` to `“`, `--` to `—`, `...` to `…`.
- **Table of contents**: Inserted using `{{TOC}}`. `{{TOC:2-3}}` limits it to levels 2 and 3.


It also broadens the default [[Markdown table|table]] syntax:
```
|             |          Grouping           ||
First Header  | Second Header | Third Header |
 ------------ | :-----------: | -----------: |
Content       |          *Long Cell*        ||
Content       |   **Cell**    |         Cell |

New section   |     More      |         Data |
And more      | With an escaped '\|'         ||  
```




