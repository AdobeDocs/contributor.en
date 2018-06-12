---
title: How to use Markdown for writing Docs
description: This article provides the basics and reference information for the Markdown language used for writing articles.
---
# How to use Markdown for writing Docs

Adobe Docs articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn. 

Because Adobe Docs content is stored in GitHub, it can use a version of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs. Additionally, Adobe extended Markdown in a few ways to support certain help-related features such as notes and embedded videos.

## Markdown basics

### Headings

To create a heading, you use a hash mark (#), as follows:

```markdown
    # This is level 1 (article title)
    ## This is level 2
    ### This is level 3
    #### This is level 4
```

### Basic text

To format text as **bold**, you enclose it in two asterisks:

```markdown
    This text is **bold**.
```

To format text as *italic*, you enclose it in a single asterisk:

```markdown
    This text is *italic*.
```

To format text as both ***bold and italic***, you enclose it in three asterisks:

```markdown
    This is text is both ***bold and italic***.
```

To format superscript (H<sub>2</sub>O) and subscript (e=mc<sup>2</sup>) text:

```markdown
This is subscript H<sub>2</sub>O and superscript e=mc<sup>2</sup>.
```

To ignore Markdown formatting characters, use \ before the character:

```markdown
This is not \*italicized\* type.
```

```markdown
    To create an indent, press Tab or add four spaces at the beginning of the paragraph.
```

    To create an indent, press Tab or add four spaces at the beginning of the paragraph.

### Lists

#### Unordered list

To format an unordered/bulleted list, you can use either asterisks or dashes. For example, the following Markdown:

```markdown
- List item 1
- List item 2
- List item 3
```

will be rendered as:

- List item 1
- List item 2
- List item 3

To nest content within list items, indent the child list items. For example, the following Markdown:

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

will be rendered as:

- List item 1
  - List item A
  - List item B
- List item 2

#### Ordered list

To format an ordered list, you use corresponding numbers. For example, the following Markdown:

```markdown
1. Step 1
1. Step 2
1. Step 3
```

will be rendered as:

1. Step 1
1. Step 2
1. Step 3

To nest content within list items, indent the child list items. For example, the following Markdown:

```markdown
1. Do this.
    Explanation of step.
1. Do that.
    > ![Image](/assets/adobe_logo.png)
1. Do the other.
```

will be rendered as:

1. Do this.
    Explanation of step.
1. Do that.
    > ![Image](/assets/adobe_logo2.png)
1. Do the other.

### Tables

Tables are not part of the core Markdown specification, but Adobe supports them. You can create tables by using the pipe (|) character to delineate columns and rows. Hyphens create each column's header, while pipes separate each column. Include a blank line before your table so it's rendered correctly.

For example, the following Markdown:

```markdown
| Left                 | Center              | Right            |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

will be rendered as:

| Left                 | Center              | Right            |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

For more information on creating tables, see:

- The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables
- GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)
- The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app
- [Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table)
- [Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/)

### Links

The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:

 `[link text](file-name.md)`

For more information on linking, see:

- The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.
- The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that Markdig provides.

### Code snippets

Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences. For details, see:

- [Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)
- [GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

Fenced code blocks are an easy way to enable syntax highlighting for your code snippets. The general format for fenced code blocks is:

    ```alias
    ...
    your code goes in here
    ...
    ```

The alias after the initial three backtick (`) characters defines the syntax highlighting to be used. The following is a list of commonly used programming languages in Docs content and the matching label:

These languages have friendly name support and most have language highlighting.

|Name|Markdown Label|
|-----|-------|
|.NET Console|dotnetcli|
|ASP.NET (C#)|aspx-csharp|
|ASP.NET (VB)|aspx-vb|
|AzCopy|azcopy|
|Azure CLI|azurecli|
|Azure PowerShell|azurepowershell|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|CSHTML|cshtml|
|DAX|dax|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Markdown|md|
|NodeJS|nodejs|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|Power Apps Formula|powerappsfl|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|VSTS CLI|vstscli|
|XAML|xaml|
|XML|xml|

#### Example: C\#

__Markdown__

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

__Render__

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### Example: SQL

__Markdown__

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

__Render__

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## OPS custom Markdown extensions

> [!NOTE]
> Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM). Markdig adds some functionality through Markdown extensions. As such, selected articles from the full OPS Authoring Guide are included in this guide for reference. (For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)

Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings. For richer formatting, articles can use Markdig features such as:

- Note blocks
- Includes
- Selectors
- Embedded videos
- Code snippets/samples

For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.

### Note blocks

You can choose from four types of note blocks to draw attention to specific content:

- NOTE
- WARNING
- TIP
- IMPORTANT

In general, note blocks should be used sparingly because they can be disruptive. Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.

## Gotchas and troubleshooting

### Alt text

Alt text that contains underscores won't be rendered properly. For example, instead of using this:

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

Escape the underscores like this:

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### Apostrophes and quotation marks

If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks. These need to be encoded or changed to basic apostrophes or quotation marks. Otherwise, you end up with things like this when the file is published: Itâ€™s

Here are the encodings for the "smart" versions of these punctuation marks:

- Left (opening) quotation mark: `&#8220;`
- Right (closing) quotation mark: `&#8221;`
- Right (closing) single quotation mark or apostrophe: `&#8217;`
- Left (opening) single quotation mark (rarely used): `&#8216;`

### Angle brackets

If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets. Otherwise, Markdown thinks that they're intended to be an HTML tag.

For example, encode `<script name>` as `&lt;script name&gt;`

### Ampersands in titles

Ampersands (&) aren't allowed in titles. Use "and" instead, or use the `&amp;` encoding.

## See also

### Markdown resources

- [Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)
- [Docs Markdown cheat sheet](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [GitHub's Markdown Basics](https://help.github.com/articles/markdown-basics/)
