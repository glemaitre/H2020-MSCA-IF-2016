Latex Template for H2020-MSCA-IF-2015 application
=================================================

This is a LaTeX template for the Marie Sklodowska-Curie Individual Fellowships application (H2020-MSCA-IF-2015).

Call Information
----------------
Specific Call information can be found [here](https://ec.europa.eu/research/participants/portal4/desktop/en/opportunities/h2020/calls/h2020-msca-if-2015.html)

### Important dates
(check-list to keep track of the dates)

* [x] **2015-Mar-12** Opening Date
* [ ] **2015-Sep-12 17:00 (GMT+2)** Deadline

### Submission Guidelines
(check-list to ensure proper submission)
* [x] Register to ECAS
* [x] Register the PRE-proposal (see [manual](https://webgate.ec.europa.eu/fpfis/wikis/display/ECResearchGMS/Steps+1+and+2+Logging+in+and+Selecting+a+Topic?src=email))
  * Select the topic H2020-MSCAIF-2015
  * Find the PIC number for your institution (`UdG PIC is: 999895983`)
  * the ACRONYM you want for your project title
  * Add people who needs to access to the proposal 
      * Jordi Castanyer (european.office@udg.edu)
* [ ] Prepare **part B** documentation using this template
  * [ ] 10 pages limit for sections 1-3 all together
  * [ ] No reference to the outmcome of previous evaluations of this or any similar proposal should be included in the text. Experts will be strictly instructed to disregard any such references.
  * Sections:
    * [ ] Excellence
    * [ ] Impact
    * [ ] Implementation
    * [ ] CV
    * [ ] Capacities of the participating organizations
    * [ ] Ethical aspects
* [ ] H2020-MSCA-IF-2015 application **Formularie**
  * [ ] Download
  * [ ] Fill
  * [ ] Upuload
* [ ] Upuload **part B**
* [ ] Check application
* [ ] Validate

About the Template
------------------

This template is based on the following two:

* [H2020-MSCA-IF-2014](https://github.com/dreixel/IEF-PartB) by @dreixel
* [Reserach publication](https://github.com/massich/research_pub) by @i2cvb


As in the original project's disclamer:
I do not offer any guaratees about this template. In particular, I cannot assure you that it fits the required guidelines (although I have tried to make it so).

Colaboration
------------

Feel free to open a pull request if you would like to improve this template!

### Structure
The primary file is called main.tex, and contains the bare essential and the abstract to get an idea of the content at a glance. The content is imported using include and input. Latex packages, acronyms, etc.. are called using input directly meanwhile the chapters (or sections) are called using include. If a chapter source requires from an external file, this is imported using input (in the further included chapter file).

The document structure is as follows
```
    .
    |____.gitattributes       % indicates git how to treat pdf and latex files
    |____.gitignore           % indicates git which files to ignore
    |____.git
    | |__ % Contains all the info regarding the repository
    |
    |____main.pdf             % document output
    |____main.tex             % document source
    |____README.md            % this document you are reading.
    |
    |____content/
    | |   % This folder contains any file related with the content of the
    | |   % document. Each capter (or section) are stored in separated
    | |   % folders, which contain a figures subdirectory. Other content
    | |   % refering to the whole document such as frontmatter, acronyms
    | |   % and bibliography can be found directly in this content folder.
    | |
    | |____acronym_definition.tex
    | |____frontmatter.tex                  % Title, author, etc..
    | |____literature_review.bib
    | |
    | |____proposal/
    | | |____content/
    | | |   % This folder contains the figures, and files to generate the
    | | |   % these figures in case the figures are .tex
    | | |
    | | |____excelence.tex
    | | |____impact.tex
    | | |____implementation.tex
    | |
    | |____cv/
    | |____org/
    | |____ethical/
    | |
    | |____other
    | | |____cite_examples.tex              % how-to use biblatex
    | | |____other.tex
    |
    |____latex
    | |   % This folder contains all the files regarding the behaviour of
    | |   % the document. Filesystem contains packages, styles, etc..
    | |   % If fonts or other resources are needed they must be found here
    | |
    | |____filesystem
    | | |____package.tex
    | | |____fileSetup.tex
    | |____fonts
```

### Latex Packages
The cross indicates, that they have a usage example in this template.

* [ ] [biblatex](http://www.ctan.org/pkg/biblatex) using a biber backend
* [ ] graphicx
* [x] newclude
* [ ] acro using marcos=true, which allow for \myTriger instead of \ac{myTriger}
* [x] hyperref
* [ ] cleveref
* [ ] lipsum


### Procedure
The master branch should be stay clean. Every conceptual increment (or todo item) should generate an issue. In order to address the issue a branch should be created and worked out. Once the issue is finished the master is checked out and the branch merged. If a issue needs to be reopen the issue is checked out, merged to master and reworked. Consider to open a new issue instead of reopening a previous one when possible.

### LaTeX Copmpilation

* Usual latex run

  ```
  latex master
  biber master
  latex master
  latex master
  ```

* Automated compilation with preview (my choice, using *latexmk* and *xelatex*)

  ```
  latexmk --xelatex -pvc --pdf master.tex
  ```

### Important Note:
Keeping this file updated is important, it can help in further projects.

TODO
----
(Stuff to get done, either in the project or the template, that would depend :))

* [ ] Use **titling** package for the starting and ending page
* [ ] Test packages with by adding a usege example
* [ ] Task 1
* [ ] Task 2
