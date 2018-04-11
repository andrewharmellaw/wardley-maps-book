# Contributing

Contributing is easy, and we welcome your input.  Contributions will typically in the form of corrections, or additions (new chapters.)

To make a contribution, please fork the repo, make your changes, and submit them as a pull request.  We'll then review them and merge if appropriate.  (You might get some comments/feedback on things to change to your submission. Please take these in the spirit in which they are intended - to make the end result a handy resource, and true to the spirit of the original posts.)

Thanks for your input!

# My porting workflow
To "port" a chapter I do the following:
1. Cut and paste the Chapter post into a new Google Doc
1. Set the title to be a "Title", and headings to be Heading 1, Heading 2, etc as appropriate 
1. Use the [Asciidoc Processor Google Docs plugin](https://chrome.google.com/webstore/detail/asciidoc-processor/eghlmnhjljbjodpeehjjcgfcjegcfbhk?hl=en) to generate the AsciiDoc version of the document
1. Copy the generated result, and paste it into a new .doc file
1. Save the file with the name ```chapter-N-CHAPTER-TITLE.adoc```
1. Add the chapter anchor at the top (see existing chapters for what this looks like)
1. Add newlines after every ```+``` character
1. Download all the images from the chapter and put them in the "images" directory
1. Replace every "Figure X ..." with the image title / link / anchor etc. (see existing chapters for what this looks like)
1. Replace the links to other chapters / figures with ```xrefs``` (cross-references)
1. Add the chapter to the spine file (```wardley-maps-book.adoc```)
1. Remove the todo from the list below for the chapter you just ported
