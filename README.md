# WELCOME TO THE SMITH PSYCHOLOGY CLUB RESOURCE WEBSITE

This README.md file will serve as a guide to future students attempting to make edits to the website. 
Hopefully this guide helps anyone feel confident working in github pages: it may look intimidating, but it's really quite simple :)

## Descriptions of each page
Firstly, each page is its own markdown (.md) file contained in this repository. Psych majors: if you've taken statistics and used 
R Studio, you've likely used markdown before. No worries if you have not, it is easy to get the hang of either way. Here is a markdown 
"cheat sheet" that you may find helpful in making edits to these pages: https://www.markdownguide.org/cheat-sheet/ 

Each markdown file starts with what is called YAML front matter. This essentially controls the CODE for what the markdown content calls. 
This has things like page title, permalink (how you call the page in code), layout specifiers, etc. This corresponds to the primary YAML
file for this website, **_config.yml**. This file controls the code for the entire website, and the YAML header stitches the individual 
pages to the overall site.

### Home page
The home page is a splash page. This file is called **index.md**. 

### How to navigate 
The 'how to navigate' page is called **about.md** and is located in the _pages directory.

### Academics
The 'academics' page is called **academics.md** and is located in the _pages directory.

### Extracurricular
The 'extracurricular' page is called **extracurricular.md** and is located in the _pages directory.

This site was made following the minimal mistakes guide for creating a github pages website. Minimal mistakes is a jekyll theme. You can
reference this website: https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/ as a guide for how to add certain features.

## Descriptions of the directories
Directories are the little folders contained in this repository.

## _assets
This directory holds web content like images or files. 

## _data
This directory has one document, **_navigation.yml** which controls what pages are displayed in the top navigation bar. If you want to add a 
new page, follow the outline of the others in this document. They'll connect to the .md pages in the _pages directory by using the permalink.
