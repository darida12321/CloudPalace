---
cssclasses:
  - table-valign-center
---
Markdown is a markup language that uses [[String representation|text]] for formatting a document. It's not a [[WYSIWYG]] editor. It has a [[String representation|text]]-based format, and an [[HTML|HTML]]-based output. However, even if its text format, it is quite readable.

After its creation in 2004, a lot of other implementations popped up adding extra features. Some were slowly added back into the main specification as well, but some where left intentionally unspecified, as different sites have different needs.

# How it works
Under the hood, there is a multi-step process being executed.
1. Create a `.md` or `.markdown` plain [[String representation|text]] file.
2. Open a **markdown app** and point it to the file.
3. The **markdown processor** (or **parser** or **implementation**) will convert it to a [[HTML]] doc.
4. View the [[HTML|HTML]] file using another app like a browser or [[Obsidian|obsidian]].

# Features
There is no universal set of accepted **markdown features**. Each application implements their own version of markdown. These are called **flavours**.

There are some basic features that almost every markdown parser implements.
```tx
| Markdown | Result |
| --- | --- |
| [[Markdown headings\|Headings]] | `# Heading` |
| [[Markdown styles\|Styles]] | `**Bold**, *italic*, etc.` |
| [[Markdown horizontal rule\|Horizontal rule]] | `---` |
| [[Markdown code block\|Code block]] | `    Indented code` |
| [[Markdown quote blocks\|Quote blocks]] | `> Quote` |
| [[Markdown lists\|Lists]] | `- List` |
| [[Markdown definition list\|Definition list]] | `: definition` |
| [[Markdown image\|Images]] | `![markdown\|50](/Admin/Attachments/Markdown_logo.png)` |
| [[Markdown links\|Links]] | `[Markdown](https://www.markdownguide.org)` |
| [[Markdown HTML\|HTML]] | `<em>bold<\em>` |
```
There are some extended features that are implemented less often.
```tx
| Markdown | Result |
| --- | --- |
| [[Markdown table\|Tables]] | <code>\| Header 1 \| Header 2 \|<br>\| -------- \| -------- \|<br>\| Item 1   \| Item 2   \|<br>\| Item 3   \| Item 4   \|</code> |

| [[Markdown fenced code block\|Code blocks]] |    ``` |\
|                                             |    Hello world! |\
|                                             |    ``` |
| [[Markdown footnote\|Footnotes]] | `A footnote[^1]` |
| [[Markdown heading ID\|Heading IDs]] | `# My header {#my-id}` |
| [[Markdown task list\|Task lists]] | `- [ ] Task` |

```
Of course, many parsers decide to implement completely novel features too.

# Examples
Some notable **flavours** are used by [[Obsidian markdown|Obsidian]], [[Discord markdown|Discord]], [[Github markdown|Github]], [[MultiMarkdown|MultiMarkdown]], etc...
A more comprehensive list can be found [here](https://www.markdownguide.org/tools/).

