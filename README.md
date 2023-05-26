[![Latex](https://img.shields.io/badge/Made%20with-LaTeX-1f425f.svg)](https://en.wikipedia.org/wiki/LaTeX)

# LaTeX template for a thesis at MRM Materials Engineering

## How to fill the template
The template provides a basic structure for a thesis. Your edits will change primarily those fields, which are currently orange. For more information on LaTeX, also take a look at the [MRM Hub](https://mrmhub.mrm.uni-augsburg.de/index.php?r=wiki%2Fpage%2Fview&title=LaTeX&cguid=1fab046e-9c7c-41f9-b982-a200c3f1c54a).

You may start by adding the basic information to `templates/metadata.tex`. This includes the type of thesis, your address, your supervisor names, etc. You should replace all orange entries, for example `\textcolor{orange}{Thesis type}` with `Bachelor's thesis`.

If applicable, you may replace the orange text in the file `expose.tex` to write a short summary of your task at the beginning of your thesis. Writing the Exposé gives you an ooportunity to formulate the scope of the thesis in your own words. Stating a clear scope helps to prevent potential misunderstandings with your supervisor and can help you to structure your work. 

The thesis itself is built with the file `thesis.tex`. This document is just a wrapper to include various files, in wich you write the actual text. Therefore you should edit the individual files in the directories `templates` and `chapters` based on the instructions provided in orange text color.

### Length of the document
Guidelines for the length of the written version of a Bachelor's or Master's thesis are listed in the table.
The number of pages refers to the main part (introduction to outlook). This means that the appendix, list of abbreviations, etc. are not taken into account.
Larger deviations from the guideline values should be avoided and discussed with the respective supervisor.
The basic part should not exceed a quarter of the number of pages of the written version.

|             | Pages (Introduction to conclusion) |
| ----------- | ---------------------------------- |
| Lab Project | 20 - 40 Pages                      |
| Bachelor    | 40 - 70 Pages                      |
| Master      | 70 - 100 Pages                     |

## Repository
This repository includes the latest LaTex template for theses at the Chair of Materials Engineering. Students can be added as members of the repository (Settings -> Members) with guest privileges after logging in at least once at [git.rz-uni-augsburg.de](git.rz-uni-augsburg.de).
Then there are two options:

### Local computer 
Create a fork for the thesis (project page -> fork -> own account) or simply download the template. 
You may then compile the document on your local computer with 
```
    latexmk -pdf thesis.tex
```
or 
```
    latexmk -pdf expose.tex
```

This requires you to install LaTeX and the required packages on your local computer.

### Overleaf
You may also use the online editor [Overleaf](https://www.overleaf.com/) without installation on your machine. To do so, download the template and upload it to Overleaf as a new project (Overleaf -> New Project -> Upload Project) or clone it directly from https://www.overleaf.com/read/pmhrbthfckqk. 