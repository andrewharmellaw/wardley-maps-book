# Welcome
This is an Asciidoc book of Simon Wardley's "Wardley Maps". It simply takes all his [medium posts](https://medium.com/wardleymaps) and joins them together for ease of reading.  The intention is to be entirely faithful to the original posts - I've not even fixed the few spelling mistakes - while allowing various output versions to be generated, e.g. HTML, and .mobi for Kindle e-readers.  It is made available under the same Creative Commons Attribution-ShareAlike-4.0-International licence as the original posts. 

# Downloads
If you want the PDF, or MOBI versions of this book, click on the "releases" tab above.

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

# Contributing
Contributions are cool, and also very welcome.  There is a [code of conduct](CODE_OF_CONDUCT.md), and a [contribution guide](CONTRIBUTING.md) which you can familiarise yourself with if you want to get involved (even if its just fixing a typo).  They should be _very_ unsurprising to anyone used to the OSS world.

# To Do
* Fix xref rendering on .mobi (Kindle) file generation - it doesn't work
* Replace the formulae image in chapter 19 with the latex equivalent (https://github.com/asciidoctor/asciidoctor-latex)
* Change the type-setting so that paragraphs in the ```.mobi``` output aren't indented
* Add a Travis build
