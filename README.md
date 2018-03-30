# Welcome
This is an Asciidoc book of Simon Wardley's "Wardley Maps". It simply takes all his [medium posts](https://medium.com/wardleymaps) and joins them together for ease of reading.  The intention is to be entirely faithful to the original posts - I've not even fixed the few spelling mistakes - while allowing various output versions to be generated, e.g. HTML, and .mobi for Kindle e-readers.  It is made available under the same Creative Commons Attribution-ShareAlike-4.0-International licence as the original posts. 

# Downloads
Once I've tested them, there will be downloads of .pdf and .mobi files on the "Releases" tab.  

# Generating the book yourself
All these generators require you to have installed [asciidoctor](https://asciidoctor.org/docs/user-manual/). Then select the command you require to generate the output you desire.

## HTML 
To generate the HTML version of this book, run the following command in the base directory of this repository:

    asciidoctor wardley-maps-book.adoc

## PDF
To generate the PDF version of this book, you additionally need to install [asciidoctor-pdf](https://asciidoctor.cn/docs/convert-asciidoc-to-pdf/) with the following command:

    gem install --pre asciidoctor-pdf

Then you can run the following command in the base directory of this repository:

    asciidoctor-pdf wardley-maps-book.adoc

## .MOBI (Kindle)
To generate the .mobi version of this book you additionally need to install [Asciidoctor-EPUB3](https://asciidoctor.org/docs/asciidoctor-epub3/) and [kindlegen](https://rubygems.org/gems/kindlegen/versions/3.0.3) both via  Ruby gems - the instructions are in the linked pages.  The pre-requisite to run both of these is Ruby. You can then run the following command in the base directory of this repository:

    asciidoctor-epub3 -a ebook-format=kf8 wardley-maps-book.adoc

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
1. Add the chapter to the spine file (```wardley-maps-book.adoc```) and up the minor version number to be the same as the chapter you're adding
1. Remove the todo from the list below for the chapter you just ported

# To Do
* Fix xref rendering on .mobi (Kindle) file generation - it doesn't work
* Replace the formulae in chapter 19 with the latex equivalent (https://github.com/asciidoctor/asciidoctor-latex)
* Add a cover
* Change the type-setting so that paragraphs in the ```.mobi``` output aren't indented
* Add a Travis build
