# Welcome
This is an Asciidoc book of Simon Wardley's "Wardley Maps". It simply takes all his [medium posts](https://medium.com/wardleymaps) and joins them together for ease of reading.  The intention is to be entirely faithful to the original posts - I've not even fixed the few spelling mistakes - while allowing various output versions to be generated, e.g. HTML, and .mobi for Kindle e-readers.  It is made available under the same Creative Commons Attribution-ShareAlike-4.0-International licence as the original posts. 

# Generating the book yourself
To generate the HTML version of this book, you need to have installed [asciidoctor](https://asciidoctor.org/docs/user-manual/), and then you can run the following command in the base directory of this repository:

    asciidoctor wardley-maps-book.adoc

To generate the .mobi version of this book you additionally need to install [Asciidoctor-EPUB3](https://asciidoctor.org/docs/asciidoctor-epub3/) and [kindlegen](https://rubygems.org/gems/kindlegen/versions/3.0.3) both via  Ruby gems - the instructions are in the linked pages.  The pre-requisite to run both of these is Ruby. You can then run the following command in the base directory of this repository:

    asciidoctor-epub3 -a ebook-format=kf8 wardley-maps-book.adoc

# To Do
* Port chapter 9
* Port chapter 10
* Port chapter 11
* Port chapter 12
* Port chapter 13
* Port chapter 14
* Port chapter 15
* Port chapter 16
* Port chapter 17
* Port chapter 18
* Port chapter 19
* Fix xref rendering on .mobi (Kindle) file generation - it doesn't work
* Add a cover
* Change the type-setting so that paragraphs in the ```.mobi``` output aren't indented
* Add a Travis build
