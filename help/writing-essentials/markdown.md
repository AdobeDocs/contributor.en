---
title: How to use Markdown for writing documentation
description: Learn the basics of Markdown authoring. Find reference information for the Markdown language used for writing articles.
exl-id: 3e5726e2-139e-4e44-ae5b-8a3ae4782faf
---
# How to use Markdown for writing technical documentation

Adobe technical documentation articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn. 

As we are storing Adobe Docs content in GitHub, it can use a version of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs. Additionally, Adobe extended Markdown in a few ways to support certain help-related features such as notes, tips, and embedded videos.

## Markdown basics

The following sections describe the basics of authoring in Markdown.

### Headings

To create a heading, use a hash mark (#) at the beginning of a line:

```
# This is level 1 (article title)
## This is level 2
### This is level 3
#### This is level 4
##### This is level 5
```

### Basic text

A paragraph requires no special syntax in Markdown.

To format text as **bold**, you enclose it in two asterisks. To format text as *italic*, you enclose it in a single asterisk:

```markdown
   This text is **bold**.
   This text is *italic*.
   This text is both ***bold and italic***.
```

To ignore Markdown formatting characters, use \ before the character:

```markdown
This is not \*italicized\* type.
```

### Numbered lists and bullet lists

To create numbered lists, begin a line with `1.` or `1)`, but don't use both formats within the same list. You don't need to specify the numbers. GitHub does that for you.

```markdown
1. This is step 1.
1. This is the next step.
1. This is yet another step, the third.
```

Displayed:

1. This is step 1.
1. This is the next step.
1. This is yet another step, the third.

To create bullet lists, begin a line with \* or - or +, but don't mix the formats within the same list. (Do not mix bullet formats, such as \* and \+, within the same document.)

```markdown
* First item in an unordered list.
* Another item.
* Here we go again.
```

Displayed:

* First item in an unordered list.
* Another item.
* Here we go again.

You can also embed lists within lists and add content between list items.

```markdown
1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/no-localize/adobe_standard_logo.png)
1. Make sure that your table looks like this: 

   | Hello | World |
   |---|---|
   | How | are you? |  
1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.

1. Do another step.
```

Displayed:

1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/no-localize/adobe_standard_logo.png)
1. Make sure that your table looks like this: 

   | Hello | World |
   |---|---|
   | How | are you? |  
1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.

1. Do another step.

### Tables

Tables are not part of the core Markdown specification, but Adobe supports them to an extent. Markdown doesn't support multiple lines lists in cells. Best practice is to avoid using multiple lines in tables. You can create tables by using the pipe (|) character to delineate columns and rows. Hyphens create each column's header, while pipes separate each column. Include a blank line before your table so it's rendered correctly.

```markdown
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

Displayed:

| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |

Simple tables work adequately in Markdown. However, tables that include multiple paragraphs or lists within a cell are difficult to work with. For such content, we recommend using a different format, such as headings & text.

For more information on creating tables, see:

* GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)
* The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app
* [Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/)

### Links

The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:

`[link text](file-name.md)`

```markdown
[Adobe](https://www.adobe.com)
```

Displayed:

[Adobe](https://www.adobe.com)

For links to articles (cross-references) within the repository, use relative links. You can use all relative link operands, such as ./ (current directory), ../ (back one directory), and ../../ (back two directories).

```markdown
See [Overview example article](../../overview.md)
```

For more information on linking, see the [Links](linking.md) article of this guide for linking syntax.

### Images

```markdown
![Adobe Logo](assets/no-localize/adobe_standard_logo.png "Hover text")
```

Displayed:

![Adobe Logo](assets/no-localize/adobe_standard_logo.png "Hover text")

**NOTE:** For images that should not be localized, create a separate `do-not-localize` folder in the assets folder. Typically, images without text or images containing only sample content would be placed there. This removes any "noise" from the assets folder and reduces the amount of questions.

### Code blocks

Markdown supports the placement of code blocks both inline in a sentence and as a separate "fenced" block between sentences. For details, see [Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)

Use back ticks (`` ` ``) to create inline code styles within a paragraph. To create a specific multi-line code block, add three back ticks (` ``` `) before and after the code block (called a "fenced code block" in Markdown and just a "code block" component in AEM). For fenced code blocks, add the code language after the first set of back ticks so that Markdown correctly highlights code syntax. Example: ` ```javascript`

Examples:

```markdown
This is `inline code` within a paragraph of text.
```

Displayed:

This is `inline code` within a paragraph of text.

This is a fenced code block:

```javascript
function test() {
 console.log("notice the blank line before this function?");
```

## Custom Markdown extensions

Adobe articles use standard Markdown for most article formatting, such as paragraphs, links, lists, and headings. For richer formatting, articles can use extended Markdown features such as:

* Note blocks
* Embedded videos
* Do not localize
* Component properties, such as assigning a different heading ID to a heading

Use the Markdown block quote ( > ) at the beginning of every line to tie together an extended component, such as a note. If you need to use subcomponents within components, add an extra level of block quotes (>  >) for that subcomponent section. For example, a NOTE within a DONOTLOCALIZE section should begin with >    >.

Some common Markdown elements such as headings and code blocks include extended properties. If you need to change default properties, add the parameters in french braces /{ /} after the component. Extended properties are described in context.

### Note blocks

You can choose from these types of note blocks to draw attention to specific content:

* `[!NOTE]`
* `[!TIP]`
* `[!IMPORTANT]`
* `[!CAUTION]`
* `[!WARNING]`
* `[!ADMINISTRATION]`
* `[!AVAILABILITY]`
* `[!PREREQUISITES]`

In general, note blocks should be used sparingly because they can be disruptive. Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.


```markdown
>[!NOTE]
>
>This is a standard NOTE block.
```

Displayed:

>[!NOTE]
>
>This is a standard NOTE block.

```markdown
>[!TIP]
>
>This is a standard tip.
```

Displayed:

>[!TIP]
>
>This is a standard tip.

### Videos

Embedded videos won't natively render in Markdown, but you can use this Markdown extension.

```markdown
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

Displayed:

>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)

### More Like This

The "More Like This" component in AEM appears at the end of an article. It displays related links. When the article is rendered, it can be formatted the same as level-2 headings (##) without being added to the mini-TOC.

```markdown
>[!MORELIKETHIS]
>* [Article 1](https://helpx.adobe.com/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/support/audience-manager.html)
```

Displayed:

>[!MORELIKETHIS]
>* [Article 1](https://helpx.adobe.com/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/support/audience-manager.html)

### UICONTROL and DNL

All of our Markdown help content is localized using machine translation initially. If the help has never been localized, then we keep the machine translation. However, if the help content has been localized in the past, then the machine translated content will act as a placeholder while the content is in the process of human translation. 

**`[!UICONTROL]`**

During machine translation, items tagged with `[!UICONTROL]` are checked against a localization database for the appropriate translation. In the case that the UI is not localized, this tag will allow the system to leave the UI reference in English for that particular language (ie. Analytics references in Italian).

**Example:**

1. Go to the **[!UICONTROL Run Process]** screen.
1. Choose **[!UICONTROL File > Print > Print All]** to print all the files on your server.
1. The [!UICONTROL Processing Rules] dialog box appears.

**Source:**

```markdown
1. Go to the **[!UICONTROL Run Process]** screen.
1. Choose **[!UICONTROL File > Print > Print All]** to print all the files on your server.
1. The [!UICONTROL Processing Rules] dialog box appears.
```

**NOTE:** Of the three tagging options, this is the most crucial to deliver high quality and is mandatory.

**`[!DNL]`**

As a rule, we use a "Do not translate" list to tell the machine translation engines what to keep in English. The most prevalent items would be the long solution names like "Adobe Analytics", "Adobe Campaign", and "Adobe Target". However, there may be cases where we need to force the engine to use English because the term in question may be used in a specific or general way. This most obvious case would be short names for the solutions like "Analytics", "Campaign", "Target" etc. It would be difficult for a machine to understand that these are solution names and not general terms. The tag may also be used for third-party names/features which always remain in English or for shorter sections of text like a phrase or sentence which must remain in English.

**Example:**

* With [!DNL Target], you can create A/B tests to find the optimal 
* Adobe Analytics is a powerful solution to collect analytics on your site. [!DNL Analytics] can also help you with reporting to easily digest that data.

**Source:**

```markdown
* With [!DNL Target], you can create A/B tests to find the optimal 
* Adobe Analytics is a powerful solution to collect analytics on your site. [!DNL Analytics] can also help you with reporting to easily digest that data.
```

## Gotchas and troubleshooting

### Alt text

Alt text that contains underscores won't be rendered properly. For example, instead of using this:

```markdown
![Settings_Step_2](/assets/settings_step_2.png)
```

OUr best practice is to use hyphens (-) instead of underscores (_) in filenames.

```markdown
![Settings-Step-2](/assets/settings-step-2.png)
```

### Apostrophes and quotation marks

If you copy text into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks. These need to be encoded or changed to basic apostrophes or quotation marks. Otherwise, you end up with odd characters like this when the file is published: Itâ&euro;&trade;s

Here are the encodings for the "smart" versions of these punctuation marks:

* Left (opening) quotation mark: `&#8220;`
* Right (closing) quotation mark: `&#8221;`
* Right (closing) single quotation mark or apostrophe: `&#8217;`
* Left (opening) single quotation mark (rarely used): `&#8216;`

### Angle brackets

If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets. Otherwise, Markdown thinks that they're intended to be an HTML tag.

For example, encode `<script name>` as `&lt;script name&gt;`

### Ampersands in titles

Ampersands (&) aren't allowed in titles. Use "and" instead, or use the `&amp;` encoding.

## See also

### Markdown resources

* [Introduction to Markdown](https://daringfireball.net/projects/markdown/syntax)
* [GitHub's Markdown Basics](https://help.github.com/articles/markdown-basics/)
