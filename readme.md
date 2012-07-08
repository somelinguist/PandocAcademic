# Pandoc Academic Plugin for Sublime Text 2 #

A [Sublime Text 2](http://www.sublimetext.com/2) plugin to handle [Pandoc](http://johnmacfarlane.net/pandoc/).
The plugin proposes:
sinta
- a syntax highlighting tool associated with two dark color themes,
- different snippets to quickly add Pandoc functions
- a convertion tool to transform a Pandoc file to HTML, DocX, PDF and Beamer documents.

Based on the [Pandoc Render pluging](https://github.com/jclement/SublimePandoc).


## Installation ##

The easiest way to install the package is to use the [package control manager](http://wbond.net/sublime_packages/package_control).
Go to Preferences > Package Control > Install Package and search for "Pandoc Academic".

You can also install the plugin manually. Download the latest version from Github and copy the folder into your Sublime Text 2 Packages folder.
(for instance in Linux: ~/.config/sublime-text-2/Packages).

~~~~~~~~~~~~~ {#mycode .sh}
$ git clone git://github.com/larlequin/Pandoc-Academic-Plugin.git
~~~~~~~~~~~~~~~~~~~~~~


## Dependencies ##

You need to have a working installation of [Pandoc](http://johnmacfarlane.net/pandoc/).


## Available Commands ##

### Syntax and color scheme ###

You can select the syntax for a markdown file (Pandoc) in the Menu: View > Syntax > Pandoc.
This syntax should be selected to make the conversion menu available.

The compatible color schemes are available in the Menu: Preferences > Color Scheme > Pandoc Academic > ColorScheme.

### Conversion ###

Conversions are available in the Menu: Tools > Pandoc Convert (only if pandoc is defined as syntax).
You can convert a Pandoc file to:

- HTML with automatic web browser viewing
- HTML without automatic viewing
- DocX
- PDF (via LaTeX, see Pandoc documentation)
- Beamer (via LaTeX, see Pandoc documentation)

You can also use key shortcuts to launch the conversions:

- HTML with automatic web browser viewing >   *CTL+ALT+r*
- HTML without automatic viewing          >   *CTL+ALT+h*
- DocX                                    >   *CTL+ALT+d*
- Beamer                                  >   *CTL+ALT+b*
- PDF                                     >   *CTL+SHIFT+ALT+p*



### Snippets ###

*Generic snippets:*

- co + tabulation  = snippet to add a comment (HTML format)
- bo + tabulation  = snippet to add bold text in Pandoc/Markdown (**)
- it + tabulation  = snippet to add italic text in Pandoc/Markdown (*)
- link + tabulation= snippet to add a web link in Pandoc/Markdown

*Figures and Tables:*

- img + tabulation = snippet to add a picture in Pandoc
- tab + tabulation = snippet to add a table from a file and its title (as for an article)

*Citation/bibliography snippets:*

- ci + tabulation  = snippet to add a citation in brackets [text? @citationkey]
- bib + tabulation = add the \[\[BIB]] option to the current file

*Mathematic snippets:*

- mat + tabulation = snippet to add mathematics based on LaTeX style
- pow + tabulation = snippet to add the eta squared symbol

*Other snippets:*

- not + tabulation = add a footnote
- toc + tabulation = add the \[\[TOC]] option to the current file
- temp + tabulation= add the \[\[DOCSYTLE=name]] option to the current file
- head + tabulation= add the \[\[HEADER]] option to the current file

## Pandoc Options ##

The following hints can be added in your document to flip on additional features in Pandoc:

- **\<!-- \[\[TOC]] -->**: Add a Table of Contents to the top of your output document.
- **\<!-- \[\[NUM]] -->**: Turn on numbering of sections.
- **\<!-- \[\[BIB]] -->**: Add the bibliography option to handle citation and reference (@citationkey). The bibliography file should have the same name than the pandoc file.
- **\<!-- \[\[BIBSTYLE=name]] -->**: Specify a csl bibliography style
- **\<!-- \[\[DOCSTYLE=name]] -->**: Specify a template for the convertion to HTML or DOCX or theme in Beamer
- **\<!-- \[\[HEADER]] -->**: Add the option to add a custom header for the convertion to Beamer (the file should be in the same directory than the pandoc file)


*Note:* these hints are processed by the plugin and are NOT part of Pandoc itself.


## Templates ##

The Templates could be found in the "Styles" folder in the Pandoc plugin folder (in the package folder of Sublime Text).
The version comes with a standard html and docx template (from the Pandoc Render plugin) and with an APA guideline DOCX template.