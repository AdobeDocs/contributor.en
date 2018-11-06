---
lastModified: 2018-06-28
title: Using links in documentation
seo-title: Using links in Adobe Git/Markdown documentation
description: This article provides guidance on creating links to content and images.
seo-description: This article provides guidance on creating links to content and images for Adobe documentation.
---
# Using links in documentation

This article describes using hyperlinks in documentation pages. Links are easy to add into markdown with a few varying conventions. Links point users to content in the same page, point off into other neighboring pages, or point to external sites and URLs.

> [!IMPORTANT]
> All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).

## Link to URLs

The words that you include in link text should be the title of the page that you're linking to or specific, descriptive text.

**Examples:**

- `For more information, see the [overview article](https://github.com/AdobeDocs/target.en/help/overview.md).`

- `For more details, see [Adobe Legal Concerns](https://www.adobe.com/legal).`

## Link from one article to another

To create an inline link from one article to another article within the same repository, use the following link syntax:

- An article in a directory links to another article in the same directory:

  `[link text](article-name.md)`

- An article links from a subdirectory to an article in the root directory:

  `[link text](../article-name.md)`

- An article links from a sub-subdirectory to an article in the root directory:

  `[link text](../../article-name.md)`

- An article in the root directory links to an article in a subdirectory:

  `[link text](./directory/article-name.md)`

- An article in a subdirectory links to an article in another subdirectory:

  `[link text](../directory/article-name.md)`

- An article in a sub-subdirectory links to an article in another subdirectory:

  `[link text](../../directory/article-name.md)`
  
## Link to anchors

You do not have to create anchors. They're automatically generated at publishing time for all H2 headings. The only thing you have to do is create links to the H2 (##) sections.

- To link to a heading within the same article:

  `[link](#the-text-of-the-level2-section-separated-by-hyphens)`
  
  `[Link to anchors](#links-to-anchors)`

- To link to an anchor in another article in the same subdirectory:

  `[link text](article-name.md#anchor-name)`
  
  `[Configure your profile](overview.md#getting-started)`

- To link to an anchor in another service subdirectory:

  `[link text](../directory/article-name.md#anchor-name)`
  
  `[Configure your profile](../overview.md#configure-your-profile)`

## Link to images

As a best practice, images and files are stored in an `assets` directory at the same level as the Markdown file that links to it.

- An article links to an image in the `assets` subdirectory:

  `![alt text](assets/image-name.png)`

- An article links to an image in the `assets/no-localize` subdirectory:

  `![alt text](assets/no-localize/image-name.png)`
