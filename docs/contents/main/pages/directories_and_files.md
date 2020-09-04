#Directories and files

##Project directory overview

Study the project structure with reference to <span title= "System Documentation methods">_**[this](../../../index.md)**_</span> documentation system.

```
docs
│   brand.png
│   index.md
│
├───contents
│   ├───main
│   │   ├───assets
│   │   │       docs_ss.png
│   │   │
│   │   └───pages
│   │           directories_and_files.md
│   │
│   ├───sample_documentations
│   │   └───notification
│   │       ├───assets
│   │       │       not_arch.jpg
│   │       │
│   │       └───pages
│   │           │   notification.md
│   │           │
│   │           └───database
│   │               │   overview.md
│   │               │
│   │               ├───schema
│   │               │       schema_1.md
│   │               │       schema_2.md
│   │               │       schema_3.md
│   │               │
│   │               └───users
│   │                       admin.md
│   │                       dbo.md
│   │                       guest.md
│   │                       sys.md
│   │                       user_2.md
│   │
│   ├───working_on_the_contents
│   │   ├───assets
│   │   │       test.png
│   │   │       test_wrong.png
│   │   │
│   │   └───pages
│   │       │   approach_and_practices.md
│   │       │   documentation_structure.md
│   │       │
│   │       └───component_usage
└───overrides
        main.html

```

!!! tip "Getting the tree structure"
    -   Open terminal and navigate the directory of which you want the tree structure.
    -   Type `tree` for directory tree and `tree /f` for the directory tree including all the files. 
###main

The main contents without sub contents.
For example, [What to know?](../../main/pages/what_to_know.md) page.

!!! info
    See properties under the `nav` section on `mkdocs.yml` file on the root directory for further reference.


###assets

Contains assets (eg: image) that are to be used on the current section.


###pages 

All the pages i.e. `.md` files under the current section are included in this directory.