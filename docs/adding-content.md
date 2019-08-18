# Adding Content

## Sign up for Github

If you don't already have a Github account, you won't be able to submit any comments, issues, etc., just like most Web sites and SharePOoint itself. If you have an account - you get to skip ahead!

Simply click on the Sign up link at the top right of the page to create your account.

## Create Your Markdown

The next step is to gather the content. If you want to contribute something you've already written, it will probably require a bit of conversion. The documentation here is all written in markdown and there is a [great markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) you can use if you'd like to write new content or convert something you already have.


### Convert Word Documents

If you have your content in a Word document, you can use one of several Word to markdown conversion tools:

* [Word to Markdown Converter](https://word2md.com/)
* [Writage Markdown plugin for Microsoft Word](http://www.writage.com/)

### Convert from an existing blog post

If you're starting with an existing blog post, then you may be able to convert the HTML from the post to markdown.

* [Browserling - Convert HTML to Markdown](https://www.browserling.com/tools/html-to-markdown)
* [Digital Converter - HTML To Markdown](https://digitalconverter.azurewebsites.net/HTML-to-Markdown-converter)

### Write from scratch

If you're writing new content ferom scratch, you can choose whichever editor you like. The importent thing is to write in markdown format.

* [Visual Studio Code](https://code.visualstudio.com/) is a free editor from Microsoft and is used primarily for code. It also allows you to write markdown with a preview.

---

NOTE: Many of the tools mentioned above are developed by third parties, thus we cannot vouch for them. Let us know what issues or succcesses you have in the Issues.

## Add to the Repository

If you know how to work with Github, you probably don't need this section. You will have forked the repo, edited your fork, and issued a pull request. If that sounds like Greek to you, then here's the simple route to upload a piece of content.

### Navigate to the Appropriate Location

Thew repo is organized in a set of folders. The structure will undoubtedly change over time, but look for a folder which seems to correspond with the content you want to add. For example, you might want to add your content to the [docs/making-decisions](https://github.com/SharePoint/sp-usage-docs/tree/master/docs/making-decisions) folder if it's an article about how to decide whether to use [Teams Site vs. Communication Site: Which one should I choose?](docs\making-decisions\team-site-or-communication-site.md)

### Create the New File

Near the top of the screen, you'll see a button to Create new file. When you click that button, you'll get a new file, which you can give a name and then start editing.

#### Name the file

There is only one requirement for the filename, and this is to give it an md extension. This indicates that it is a markdown document. It's just the file extension, like docx for Word docs. As for the name itself, try to use a name which is descriptive, but not too long. For portability, us a nae which has dashes to separate the words, like: my-fantastic-article.md.

#### Edit the file

You can paste in the markdown from the previous steps or type it directly into the text box. Note the Preview tab, which allows you to see what the file will look like once you've saved it.

#### Save the file

When you are done editing, scroll down to the **Commit new file** section. Add a title and comments about what you are submitting. This is information which becomes part of the pull request - basically you're talking to the people who work on the repo. At this point, you can leave the default option to **Commit directly to the master branch.**

Push the **Commit new file** button and your content is in the repo!

