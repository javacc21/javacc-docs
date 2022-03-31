The master document for this document is JavaCC21BookContainer.adoc. It contains an include macro for each chapter and those included chapter files include all the individual .adoc files that make up the sections in each chapter.

asciidoctor-pdf is used to generate the pdf output. This is a Ruby Gem that must be installed first.

The nelson-theme.yml contains some overrides of the default settings used by asciidoctor-pdf when the book PDF is generated. Mostly the changes are about fonts, font sizes, margins, etc. Basically the body text seemed a little too small and the appendix table fonts seemed a little large.

To use the nelson-theme.yml settings, it must be included on the asciidoctor-pdf command line:

asciidoctor-pdf -a pdf-theme=nelson-theme.yml <fileToConvertToPDF>

The custom theme file is formatted in YAML. The first thing the custom theme file soes is extend the default settings, so only a couple of things needed to be changed. 

If different fonts are desired, those can also be set on the command line.