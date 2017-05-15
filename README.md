# Overview

This repository contains a LaTeX template that matches the requirements of Virginia Tech's Electronic Thesis and Dissertation (ETD) repository. This template has been refactored to integrate with [scriptorium](https://github.com/jasedi/scriptorium), a MultiMarkdown based writing tool.

# Instructions

In order to use this template, please follow the installation instructions for scriptorium. Assuming it is correctly installed, this template can be installed with the following command:

```
scriptorium template -i https://github.com/jasedit/vt_prelim.git
```

A new paper can be created in the directory `$paper` by executing:

```
scriptorium new -t vt_prelim $paper
```

# Template Variables

Variables have two potential configuration points, which will be described here. The first point is the frontmatter variable name, which is used by the underlying system to identify the value at build time. The second point is the placeholder value, which can be replaced during the new command, or manually edited later. For the following description, variables will be named in the format `Variable Name, Placeholder Name - Description`

## MultiMarkdown Frontmatter
1. `latex author`,`$AUTHOR` - name of the paper author
2. `latex title`, `$TITLE` - title of the document
3. `my abstract`, `$ABSTRACT` - defines the name of the file to include directly into the LaTeX output as the abstract
4. `bibtex`, `$BIBTEX` - defines the Bibtex file to process for this document. Delete this line to eliminate bibliography support
5. `myappendices`, `$APPENDICES` - defines the name of the file to include directly into the LaTeX output as the appendices. Not required.
6. `mypackages` - If defined, includes the value of this key as a filename in the document preamble, allowing for custom packages and commands to be included

## LaTeX/Metadata Variables

These variables can be found in the `metadata.tex` file defined in a paper directory.

1. `mykeywords`, `$KEYWORDS` - Keywords which are inserted into the document for metadata purposes
2. `mycommittee`, `$COMMITTEE` - List of committee members to place on cover page. This is unfiltered, so raw LaTeX is fully supported for multi-line and odd names
3. `mylinespace` - If defined, sets the line spacing of the document using the [setspace](http://www.ctan.org/tex-archive/macros/latex/contrib/setspace/) package.
