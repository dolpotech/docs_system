#Running the docs

1. Install <a href="https://squidfunk.github.io/mkdocs-material/getting-started/" target="_blank">Material for MkDocs</a>.
    
> (!) Troubleshooting the extension installation problem"

##Possible issue
If you have already installed <a href="https://squidfunk.github.io/mkdocs-material/getting-started/" target="_blank">mkdocs</a> and then you install material-mkdocs, you might face an issue on installing `mkdocs-material extensions`.
See [this issue](https://github.com/squidfunk/mkdocs-material/issues/1450#issuecomment-583397522) on github.

Approach for resolution"
- Uninstall mkdocs.
- Install material-mkdocs.
 
> Material mkdocs-mkdocs already includes the mkdocs package. So no need to install mkdocs separately.

2. Clone the current repo.

```git clone https://github.com/dolpotech/docs_system.git```

3. Goto project directory and run `mkdocs serve`.

#Starting new docs
1. Extract `starter_Template.zip` and extract it. Rename it according to the project relevance.                
2. Goto the starter template you just extracted and run `mkdocs serve`.
3. Start preparing awesome documentations! 