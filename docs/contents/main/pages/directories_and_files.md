#Directories and files

##Project directory overview

Study the project structure with reference to <span title= "System Documentation methods">_**[this](../../../index.md)**_</span> documentation system.

```
└───docs
    ├───assets
    ├───contents
    │   ├───main
    │   │   ├───assets
    │   │   └───pages
    │   └───sections
    │       ├───templates
    │       │   ├───assets
    │       │   └───pages
    │       └───working_on_the_contents
    │           ├───assets
    │           └───pages
    |       // Other subsections
    └───overrides
```

!!! tip "Getting the tree structure"
    -   Open terminal and navigate the directory of which you want the tree structure.
    -   Type `tree` for directory tree and `tree /f` for the directory tree including all the files. 
###main

The main contents without sub contents.
For example, [What to know?](../../main/pages/what_to_know.md) page.

!!! info
    See properties under the `nav` section on `mkdocs.yml` file on the root directory for further reference.

###section

Contents with sub-contents.
For example,`Working on the contents` that contains [How to?](../../working_on_the_contents/pages/laying_out_contents.md) page.

 
###assets

Contains assets (eg: image) that are to be used on the current section.


###pages 

All the pages i.e. `.md` files under the current section are included in this directory.