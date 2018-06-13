---
title: How to use Markdown for writing Docs
description: This article provides the basics and reference information for the Markdown language used for writing articles.
---
# How to use Markdown for writing Docs

Adobe Docs articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn. 

Because Adobe Docs content is stored in GitHub, it can use a version of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs. Additionally, Adobe extended Markdown in a few ways to support certain help-related features such as notes and embedded videos.

## Markdown basics

### Headings

To create a heading, use a hash mark (#) at the beginning of a line:

```markdown
    # This is level 1 (article title)
    ## This is level 2
    ### This is level 3
    #### This is level 4
```

### Basic text

A paragraph requires no special syntax in Markdown.

To format text as **bold**, you enclose it in two asterisks. To format text as *italic*, you enclose it in a single asterisk:

```markdown
    This text is **bold**.
    This text is *italic*.
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

### Numbered lists and bullet lists

To create numbered lists, begin a line with 1. or 1), but don't use both formats within the same list, or you'll start a new list. You don't need to specify the numbers. GitHub does that for you.

```markdown
1. This is step 1.
1. This is the next step.
1. This is yet another step, the third.
```

Rendered:

1. This is step 1.
1. This is the next step.
1. This is yet another step, the third.

To create bullet lists, begin a line with * or - or +, but don't mix the formats within the same list. (If you mix the formats, such as * and +, you essentially start a new list.)

```markdown
- First item in an unordered list.
- Another item.
- Here we go again.
```

Rendered:

- First item in an unordered list.
- Another item.
- Here we go again.

You can also embed lists within lists and add content between list items.

```markdown
1. Set up your table and code blocks.
1. Perform this step.
   ![screen](/assets/core-services_96.png)
1. Make sure that your table looks like this: 
   >| Hello | World |
   >|---|---|
   >| How | are you? |  
1. This is the fourth step.
   >[!NOTE]
   >
   >This is note text.
1. Do another step.
```

Rendered:

1. Set up your table and code blocks.
1. Perform this step.
   ![screen](/assets/core-services_96.png)
1. Make sure that your table looks like this: 
   >| Hello | World |
   >|---|---|
   >| How | are you? |  
1. This is the fourth step.
   >[!NOTE]
   >
   >This is note text.
1. Do another step.

### Tables

Tables are not part of the core Markdown specification, but Adobe supports them to an extent. Markdown doesn't support multiple lines lists in cells. Best practice is to avoid using multiple lines in tables. You can create tables by using the pipe (|) character to delineate columns and rows. Hyphens create each column's header, while pipes separate each column. Include a blank line before your table so it's rendered correctly.

```markdown
| Header | Another header | Yet another header |
|------------|:---------------:|-----------------------:|
| row 1 | centered column 2 | right-aligned column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

Rendered

| Header | Another header | Yet another header |
|------------|:---------------:|-----------------------:|
| row 1 | centered column 2 | right-aligned column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |

Simple tables work adequately in Markdown. However, tables that include multiple paragraphs or lists within a cell are difficult to work with. For such content, we recommend using a different format, such as headings & text.

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

#### Remarks and comments

```markdown
<!-- standard comment code 
-->
```

Comments (remarks) do not appear in the public-facing help articles. However, comments do appear in the public-facing Markdown files that users can see and edit.

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
